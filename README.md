# winlogreport
Create a Windows Event Log filtered report and optionally send it to E-Mail (based on nelsh/winlogcheck ideas and code)


WinLogReport creates an HTML report based on XML filter syntax

Example from MSDN:

<QueryList>
  <Query Id="0" Path="Application">
    <Select Path="Application">
        *[System[(Level &lt;= 3) and 
        TimeCreated[timediff(@SystemTime) &lt;= 86400000]]]
    </Select>
    <Suppress Path="Application">
        *[System[(Level = 2)]]
    </Suppress>
    <Select Path="System">
        *[System[(Level=1  or Level=2 or Level=3) and 
        TimeCreated[timediff(@SystemTime) &lt;= 86400000]]]
    </Select>
  </Query>
</QueryList>

