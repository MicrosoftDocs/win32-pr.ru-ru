---
description: Указывает тип подтверждения, которое может произойти для объекта Иконтекстноде.
ms.assetid: 5c906548-dbf5-4448-b248-070bd43b054e
title: Перечисление Конфирматионтипе (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfirmationType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 9f89d5457e3d75bcf781a100449e4da9f8b45624af38760ca0cdda358fbf47ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936954"
---
# <a name="confirmationtype-enumeration"></a>Перечисление Конфирматионтипе

Указывает тип подтверждения, которое может произойти для объекта [**иконтекстноде**](icontextnode.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef enum ConfirmationType { 
  ConfirmationType_None                   = 0,
  ConfirmationType_NodeTypeAndProperties  = 1,
  ConfirmationType_TopBoundary            = 4
} ConfirmationType;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="ConfirmationType_None"></span><span id="confirmationtype_none"></span><span id="CONFIRMATIONTYPE_NONE"></span>**Конфирматионтипе \_ None**
</dt> <dd>

Подтверждение не применяется. [**Иинканализер**](iinkanalyzer.md) может свободно изменять контекстный узел или любой из его потомков по мере необходимости.

</dd> <dt>

<span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**Конфирматионтипе \_ нодетипеандпропертиес**
</dt> <dd>

[**Иинканализер**](iinkanalyzer.md) не может изменить тип или любые свойства указанного контекстного узла.

</dd> <dt>

<span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**Конфирматионтипе \_ топбаундари**
</dt> <dd>

[**Иинканализер**](iinkanalyzer.md) не будет выполнять операции, включая добавление рукописного ввода или слияния с другими [**контекстнодес**](icontextnodes.md), которые приводят к перемещению топбаундари за пределы текущей верхней границы. Например:

-   Приложение анализирует набор рукописных данных, и идентифицируется Параграфноде.
-   Приложение подтверждает Топбаундари этого абзаца.
-   Пользователь приложения записывает новые рукописные данные над текущим абзацем. При повторном вызове анализа новые рукописные данные не будут включены в узел подтвержденного абзаца.
-   Так как подтверждена только верхняя граница, Контекстноде может продолжать расти в других направлениях. Удаление штрихов может привести к перемещению верхней границы. Преобразование Контекстноде может привести к изменению расположения, но не позволит объединить дополнительные рукописные данные в новом месте.

Этот Конфирматионтипе применим только к узлам абзаца.

</dd> </dl>

## <a name="remarks"></a>Remarks

Значение **нодетипеандпропертиес** можно использовать только для узлов рукописного ввода и вывода рукописного текста (см. раздел [**Иконтекстноде:: GetType**](icontextnode-gettype.md)). В противном случае возвращается **E \_ INVALIDARG** из [**иконтекстноде:: Confirm**](icontextnode-confirm.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Иконтекстноде:: Confirm**](icontextnode-confirm.md)
</dt> <dt>

[**Иконтекстноде:: Confirm**](icontextnode-isconfirmed.md)
</dt> </dl>

 

 




