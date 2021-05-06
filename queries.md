SELECT  YEAR(register_at), MONTH(register_at), COUNT(*) FROM spk GROUP BY YEAR(register_at), MONTH(register_at)

SELECT
    COUNT(id),
    DATE_FORMAT(record_date, '%Y-%m-%d') AS DAY,
    DATE_FORMAT(record_date, '%Y-%m') AS MONTH,
    DATE_FORMAT(record_date, '%Y') AS YEAR

FROM
    stats
WHERE
    YEAR = 2009
GROUP BY
    DATE_FORMAT(record_date, '%Y-%m-%d ');
