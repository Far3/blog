---
title: React Component types
date: 2017-09-05 21:08:53
tags:
---
Their are a few different ways to create class methods. You can create render methods with a class method. Be a little more declarative and use ES6. Or be 'the best' and use a stateless functional component.

Destructing is typically a good idea, to make the react code less cluttered. Use stateless componenets whenever possible, functional way to use components and also offer some performance benefits.

This is the react class method
```javascript
import React from 'react'
import '../stylesheets/ui.scss'

export const WaterDayCount = React.createClass({
    decimalToPercent(decimal) {
        return ((decimal* 100) + '%')
    },
    calculateGoalProgress(total, goal) {
        return this.decimalToPercent(total/goal)
    },
    render() {
        return (
            <div className="water-day-count">
                <div className="total-days">
                    <span>Total Days: {this.props.total}</span>
                </div>
                <div className="sail-days">
                    <span>Sailing Days: {this.props.sail}</span>
                </div>
                <div className="sup-days">
                    <span>SUP Days: {this.props.sup}</span>
                </div>
                <div className="goal">
                    <span>Goal Progress: {this.calculateGoalProgress(this.props.total, this.props.goal)}</span>
                </div>
                <span>Goal: {this.props.goal}</span>                
            </div>

        )
    }
})
```

This is the ES6 component method
```javascript
import { Component } from 'react'
import '../stylesheets/ui.scss'

    const decimalToPercent = (decimal) => {
        return ((decimal* 100) + '%')
    }
    const calculateGoalProgress = (total, goal) => {
        return decimalToPercent(total/goal)
    }

export const WaterDayCount = (props) => (

        <div className="water-day-count">
            <div className="total-days">
                <span>Total Days: {props.total}</span>
            </div>
            <div className="sail-days">
                <span>Sailing Days: {props.sail}</span>
            </div>
            <div className="sup-days">
                <span>SUP Days: {props.sup}</span>
            </div>
            <div className="goal">
                <span>Goal Progress: {calculateGoalProgress(props.total, props.goal)}</span>
            </div>
            <span>Goal: {props.goal}</span>                
        </div>

    )
```

Stateless compnent method
```javascript
import { Component } from 'react'
import '../stylesheets/ui.scss'

    const decimalToPercent = (decimal) => {
        return ((decimal* 100) + '%')
    }
    const calculateGoalProgress = (total, goal) => {
        return decimalToPercent(total/goal)
    }

export const WaterDayCount = ({total, sail, sup, goal}) => (

        <div className="water-day-count">
            <div className="total-days">
                <span>Total Days: {total}</span>
            </div>
            <div className="sail-days">
                <span>Sailing Days: {sail}</span>
            </div>
            <div className="sup-days">
                <span>SUP Days: {sup}</span>
            </div>
            <div className="goal">
                <span>Goal Progress: {calculateGoalProgress(total, goal)}</span>
            </div>
            <span>Goal: {goal}</span>                
        </div>

    )
    ```