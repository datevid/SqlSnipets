### Create function:

```
create or replace function fn_if_Ruc_Return_DNI(ruc varchar, out dni varchar)
as
$$
-----------------------------------------------------------------------------------------------------
-- Nombre         : fn_if_Ruc_Return_DNI
-- Autor          : David León Vilca
-- Verion         : 2.0
-- Description  : convierte codigo del usuario es el ruc, obtiene el DNI a partir de éste
-----------------------------------------------------------------------------------------------------
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

### Delete function function:
```
drop function ifRuc;
```
