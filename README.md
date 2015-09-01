# SQL-CREATE-AUTO-INCREMENT
CREATE SEQUENCE SEQ_GEN_IDENTITY MINVALUE 1 START WITH 1 INCREMENT BY 1 CACHE 10;  create trigger [z] before insert on [userJPA] for each row when (new.[userid] is null) begin  select SEQ_GEN_IDENTITY.nextval into :new.[userid] from dual; end;  @Id @GeneratedValue(strategy = GenerationType.IDENTITY)
