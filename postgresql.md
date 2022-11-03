Create function:

```
create or replace function ifRucReturnDNI(ruc varchar, out dni varchar)
as
$$
declare

begin
    if length(ruc) = 11 then
        dni := substring(ruc from 3 for 8);
    ELSe
        dni := ruc;
    end if;

end;
$$
    language plpgsql;
```

delete function function:
```
drop function ifRuc;
```
