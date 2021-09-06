# Raman Karseka

## Contacts:

Minsk, Belarus
tel: +375-29-191-04-79
![](https://img.icons8.com/fluent/48/000000/linkedin.png)
[Raman Karseka](https://www.linkedin.com/in/karseka/)

## About

Right now my goal is to skill up in front-end development and choose grouth vector for the next couple of years.

## Skills

ReactJS / Redux / JavaScript /Bootstrap / HTML5 / CSS3 / Git

## Code sample

```
import React from "react";
import styles from "./Paginator.module.css";

const SpanBlock = ({spanText, onClick = null, boldClass = false}) =>
    <span onClick={onClick}
          className={styles.paginator + ' ' + (boldClass && styles.selectedPage)}>{spanText}</span>

const Paginator = ({currentPage, onPageChanged, ...props}) => {
    const pagesCount = Math.ceil(props.totalUsersCount / props.pageSize);
    const pages = [];
    const firstPageCallback = page => currentPage > 1 ? () => {
        onPageChanged(page)
    } : null;
    let pNumber;
    if (currentPage < 6) {
        pNumber = 2
    } else if (currentPage > (pagesCount - 5)) {
        pNumber = pagesCount - 7;
    } else {
        pNumber = currentPage - 3
    }

    for (let i = pNumber; i < pNumber + 7; i++) {
        pages.push(i);
    }


    return <div style={{margin: '10px'}}>
        <SpanBlock onClick={firstPageCallback(currentPage - 1)}
                   spanText='&laquo;'/>

        <SpanBlock boldClass={currentPage === 1} onClick={firstPageCallback(1)}
                   spanText='1'/>

        {currentPage > 5 && <SpanBlock spanText={"..."}/>}

        {pages.map(p => {
            return <SpanBlock onClick={currentPage !== p ? () => {
                onPageChanged(p)
            } : null} boldClass={currentPage === p} key={p}
                              spanText={p}/>
        })}

        {currentPage < pagesCount - 4 && <SpanBlock spanText={"..."}/>}

        <SpanBlock boldClass={currentPage === pagesCount}
                   onClick={(currentPage !== pagesCount) ? () => {
                       onPageChanged(pagesCount)
                   } : null} spanText={pagesCount}/>

        <SpanBlock onClick={(currentPage < pagesCount) ? () => {
            onPageChanged(currentPage + 1)
        } : null} spanText='&raquo;'/>

    </div>
}
export default Paginator;
```

## Last experience

- 2014-2017
  Deputy Chief Information Officer, Junix Ltd, RF
- 2017-2021
  Security operations officer, Priorbank JSC, RB

## Education

- University:

  1. Belarusian State University, FAMCS, 2013

  software engineer 2. Belarusian State Economic University, FM, 2012

  economist-manager

## Languages

English: B1+
