# pg-lock-mon-prom


Database template
```sql
CREATE SEQUENCE users_id_seq START WITH 1;

CREATE TABLE public.users
(
  id integer NOT NULL DEFAULT nextval('users_id_seq'::regclass),
  nickname text,
  balance numeric,
  CONSTRAINT "primary" PRIMARY KEY (id)
)
WITH (OIDS=FALSE);

INSERT INTO users (id, nickname, balance) VALUES (2, 'Beta', 160.0);
INSERT INTO users (id, nickname, balance) VALUES (1, 'Alpha', 260.0);
INSERT INTO users (id, nickname, balance) VALUES (3, 'Gamma', 510.50);
```
