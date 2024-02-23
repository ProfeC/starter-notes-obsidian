## Highest Priority

```dataview
TASK
FROM
  !"/resources"
WHERE 
  !completed
  AND priority = "highest"
GROUP BY file.link
```

## High Priority

```dataview
TASK
FROM
  !"/resources"
WHERE 
  !completed
  AND priority = "high"
GROUP BY file.link
```

## Medium Priority

```dataview
TASK
FROM
  (
  !"/91 - Resources" 
  OR !"/99 - Templates" 
  OR !"/90 - People"
  )
WHERE 
  !completed
  AND
  (
    !priority
    OR priority = "medium"
  )
GROUP BY file.link
SORT date desc
```

## Low Priority

```dataview
TASK
FROM
  !"/resources"
WHERE 
  !completed
  AND 
    priority = "low" 
    OR priortiy = "lowest"
  
GROUP BY file.link
```

## Lowest Priority

```dataview
TASK
FROM
  !"/resources"
WHERE 
  !completed
  AND priority = "lowest"
GROUP BY file.link
```
