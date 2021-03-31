---
title: Управление доступом (платформа фильтрации Windows)
description: В платформе фильтрации Windows (WFP) служба базовой фильтрации (BFE) реализует стандартную модель управления доступом Windows, основанную на маркерах доступа и дескрипторах безопасности.
ms.assetid: 936ad5f0-d5cd-47ed-b9e5-a7d82a4da603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0df63b6fe92b18614a7ccf205ccf826927664ee
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "104350985"
---
# <a name="access-control-windows-filtering-platform"></a>Управление доступом (платформа фильтрации Windows)

В платформе фильтрации Windows (WFP) служба базовой фильтрации (BFE) реализует стандартную [модель управления доступом Windows](/windows/desktop/SecAuthZ/access-control-model) , основанную на маркерах доступа и дескрипторах безопасности.

## <a name="access-control-model"></a>Модель контроля доступа

Дескрипторы безопасности могут быть заданы при добавлении новых объектов WFP, таких как фильтры и подслои. Дескрипторы безопасности управляются с помощью функций управления WFP **фвпм \* GetSecurityInfo0** и **фвпм \* SetSecurityInfo0**, где * *\** _ означает имя объекта WFP. Эти функции семантически идентичны функциям Windows [_ *жетсекуритинфо* *](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) и [**сетсекуритинфо**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

> [!Note]  
> Функции **фвпм \* SetSecurityInfo0** нельзя вызывать из явной транзакции.

 

> [!Note]  
> Функции **фвпм \* SetSecurityInfo0** могут вызываться только из динамического сеанса, если они используются для управления динамическим объектом, созданным в рамках одного сеанса.

 

Дескриптор безопасности по умолчанию для обработчика фильтра (объект корневого обработчика на схеме ниже) выглядит следующим образом.

-   Предоставьте **Общий \_** доступ ко всем встроенным группам администраторов.
-   Предоставьте права доступа универсального разрешения на **\_ Чтение** ( **GR) \_** универсального разрешения на **\_ выполнение** (GX) для операторов конфигурации сети.
-   Предоставьте права доступа **гргвгкс** следующим идентификаторам безопасности службы (SSID): MPSSVC (брандмауэр Windows), Напажент (агент защиты доступа к сети), PolicyAgent (агент политики IPSec), RPCSS (удаленный вызов процедур) и Вдисервицехост (узел службы диагностики).
-   Предоставьте **фвпм \_ актрл \_ Open** и **фвпм \_ актрл \_ классифицировать** всем. (Это права доступа, характерные для WFP, описанные в таблице ниже.)

Остальные дескрипторы безопасности по умолчанию являются производными через наследование.

Существуют некоторые проверки доступа, например для **фвпм \* Add0**, **фвпм \* CreateEnumHandle0**, **фвпм \* SubscribeChanges0** вызовы функций, которые не могут быть выполнены на уровне отдельных объектов. Для этих функций существуют объекты контейнеров для каждого типа объектов. Для стандартных типов объектов (например, поставщиков, выпусков, фильтров) существующие функции **фвпм \* GetSecurityInfo0** и **фвпм \* SetSecurityInfo0** перегружаются, что означает, что параметр **GUID** с нулевым значением определяет связанный контейнер. Для других типов объектов (например, сетевых событий и сопоставлений безопасности IPsec) существуют явные функции для управления сведениями о безопасности контейнера.

BFE поддерживает автоматическое наследование записей контроля доступа (ACE) избирательного списка управления доступом (DACL). BFE не поддерживает элементы ACE системного списка управления доступом (SACL). Объекты наследуют ACE от своего контейнера. Контейнеры наследуют ACE от обработчика фильтров. Пути распространения показаны на приведенной ниже схеме.

![Схема, на которой показаны пути распространения ACE, начиная с "Engine".](images/access-control.jpg)

Для стандартных типов объектов BFE применяет все универсальные и стандартные права доступа. Кроме того, WFP определяет следующие специальные права доступа.



| Право доступа к WFP                                                                                                                        | Описание                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**\_Добавление фвпм актрл \_**<br/>                                       | Требуется для добавления объекта в контейнер.<br/>                                                                                                                     |
| <span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**ФВПМ \_ актрл \_ Добавить \_ ссылку**<br/>                       | Требуется для создания связи с объектом. Например, чтобы добавить фильтр, который ссылается на выноску, вызывающий объект должен иметь \_ доступ к вызову Add Link.<br/> |
| <span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**ФВПМ \_ актрл \_ Начало \_ чтения \_ транзакция**<br/>    | Требуется для начала явной транзакции чтения.<br/>                                                                                                               |
| <span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**ФВПМ \_ актрл \_ начать \_ запись \_ транзакция**<br/> | Требуется для начала явной транзакции записи.<br/>                                                                                                              |
| <span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**\_классификация фвпм актрл \_**<br/>                        | Требуется для классификации на уровне пользовательского режима.<br/>                                                                                                               |
| <span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**\_перечисление АКТРЛ фвпм \_**<br/>                                    | Требуется для перечисления объектов в контейнере. Однако перечислитель возвращает только те объекты, к которым вызывающий объект \_ имеет \_ доступ фвпм актрл Read.<br/>              |
| <span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**ФВПМ \_ актрл \_ Open**<br/>                                    | Требуется для открытия сеанса с BFE.<br/>                                                                                                                          |
| <span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**\_Чтение фвпм актрл \_**<br/>                                    | Требуется для чтения свойств объекта.<br/>                                                                                                                      |
| <span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**\_ \_ Статистика чтения фвпм \_ актрл**<br/>                 | Требуется для чтения статистики.<br/>                                                                                                                                  |
| <span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**\_Подписка фвпм актрл \_**<br/>                     | Требуется для подписки на уведомления. Подписчики будут получать уведомления только об объектах, к которым у них есть ФВПМ \_ актрл \_ доступ на чтение.<br/>                 |
| <span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**ФВПМ \_ актрл \_ запись**<br/>                                 | Требуется для установки параметров ядра.<br/>                                                                                                                               |



 

BFE пропускает все проверки доступа для вызывающих объектов режима ядра.

Чтобы запретить администраторам блокировку из BFE, членам встроенной группы «Администраторы» всегда предоставляется **фвпм \_ актрл \_ Open** для объекта Engine. Таким образом, администратор может восстановить доступ, выполнив следующие действия.

-   Включите привилегию **SE \_ Take \_ Ownership \_ Name** .
-   Вызовите [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0). Вызов выполняется, так как участник является членом встроенных администраторов.
-   Стать владельцем объекта Engine. Это происходит успешно, так как у вызывающего объекта есть привилегия **SE \_ Take \_ Ownership \_ Name** .
-   Обновите список DACL. Это происходит успешно, так как владелец всегда имеет доступ на **запись \_ DAC** .

Так как BFE поддерживает собственный пользовательский аудит, он не создает аудиты доступа к универсальным объектам. Таким же списком SACL игнорируется.

## <a name="wfp-required-access-rights"></a>Необходимые права доступа в WFP

В приведенной ниже таблице показаны права доступа, необходимые функциям WFP для доступа к различным объектам платформы фильтрации. **Функции фвпмфилтер \* *_ перечислены в качестве примера для доступа к стандартным объектам. Все остальные функции, обращающиеся к стандартным объектам, следуют* \*** модели доступа к функциям _ фвпмфилтер.



Функция

Объект проверен

Требуемый доступ

[**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)

Подсистема

**ФВПМ \_ актрл \_ Open**

[**FwpmEngineGetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginegetoption0)

Подсистема

**\_Чтение фвпм актрл \_**

[**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)

Подсистема

**ФВПМ \_ актрл \_ запись**

[**FwpmSessionCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsessioncreateenumhandle0)

Подсистема

**\_перечисление АКТРЛ фвпм \_**

[**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)

Подсистема

**Фвпм \_ актрл \_ начать \_ Чтение \_ транзакция**  &  **фвпм \_ актрл \_ начать \_ запись \_ транзакция**

[**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

Поставщик контейнера<br/> Уровень<br/> Sub-Layer<br/> Выноска<br/> Контекст поставщика<br/>

**ФВПМ \_ актрл \_ аддфвпм \_ актрл \_ Add \_ Link**<br/> **ФВПМ \_ актрл \_ Добавить \_ ссылку**<br/> **ФВПМ \_ актрл \_ Добавить \_ ссылку**<br/> **ФВПМ \_ актрл \_ Добавить \_ ссылку**<br/> **ФВПМ \_ актрл \_ Добавить \_ ссылку**<br/>

[**FwpmFilterDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)<br/>

Фильтр

**DELETE**

[**FwpmFilterGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)<br/>

Фильтр

**\_Чтение фвпм актрл \_**

[**FwpmFilterCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltercreateenumhandle0)

Фильтр контейнера<br/>

**ФВПМ \_ актрл \_ енумфвпм \_ актрл \_ Read**<br/>

[**FwpmFilterSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscribechanges0)

Контейнер

**\_Подписка фвпм актрл \_**

[**FwpmFilterSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscriptionsget0)

Контейнер

**\_Чтение фвпм актрл \_**

[**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0)

База данных SA IPsec

**\_ \_ Статистика чтения фвпм \_ актрл**

[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)<br/> [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)<br/> [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)<br/>

База данных SA IPsec

**\_Добавление фвпм актрл \_**

[**IPsecSaContextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaContextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)<br/>

База данных SA IPsec

**DELETE**

[**IPsecSaContextGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0)

База данных SA IPsec

**\_Чтение фвпм актрл \_**

[**IPsecSaContextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)<br/>

База данных SA IPsec

**Фвпм \_ актрл \_ enum**  &  **фвпм \_ актрл \_ Read**

[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)

БАЗА ДАННЫХ IKE SA

**\_ \_ Статистика чтения фвпм \_ актрл**

[**IkeextSaDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)

БАЗА ДАННЫХ IKE SA

**DELETE**

[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0)

БАЗА ДАННЫХ IKE SA

**\_Чтение фвпм актрл \_**

[**IkeextSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)

БАЗА ДАННЫХ IKE SA

**Фвпм \_ актрл \_ enum**  &  **фвпм \_ актрл \_ Read**

[**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0)

Контейнер

**\_перечисление АКТРЛ фвпм \_**

[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)<br/>

Дополнительные проверки доступа выходят за рамки отдельных фильтров и контекстов поставщиков



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Стандартные права доступа**](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[Модель управления доступом Windows](/windows/desktop/SecAuthZ/access-control-model)
</dt> <dt>

[**Идентификаторы прав доступа платформы фильтрации Windows**](access-right-identifiers.md)
</dt> </dl>

 

