---
description: Метод DoAction объекта Session выполняет функцию действия, соответствующую указанному имени.
ms.assetid: 6cff1cf1-1c8f-4c43-a687-e927e8573e55
title: Метод Session. DoAction («фотополучение. h»)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.DoAction
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3084cfd51e7efbcfbfbc3cbcf2c9be21d8373d21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675723"
---
# <a name="sessiondoaction-method"></a>Session. DoAction, метод

Метод **DoAction** объекта [**Session**](session-object.md) выполняет функцию действия, соответствующую указанному имени. Если указано пустое имя действия, подсистема использует значение [свойства Action](action.md) в верхнем регистре в качестве выполняемого действия. Если значение свойства не определено, выполняется действие по умолчанию, которое в настоящее время определено как INSTALL. Этот метод возвращает целочисленное перечисление.

## <a name="syntax"></a>Синтаксис


```JScript
Session.DoAction(
  action
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*action* 
</dt> <dd>

Обязательное строковое имя действия, которое необходимо выполнить. С учетом регистра.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Действия, которые обновляют систему, такие как действия [инсталлфилес](installfiles-action.md) и [вритерегистривалуес](writeregistryvalues-action.md) , не могут быть запущены путем вызова метода **DoAction** . Исключением из этого правила является то, что метод **DoAction** вызывается из настраиваемого действия, запланированного в [таблице инсталлексекутесекуенце](installexecutesequence-table.md) между [действиями](installfinalize-action.md) [инсталлинитиализе](installinitialize-action.md) и функции InstallFinalize. Действия, которые не обновляют систему, например [аппсеарч](appsearch-action.md) или [костинитиализе](costinitialize-action.md), могут быть вызваны.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| Header<br/>  | <dl> <dt>Фотоприобретение. h</dt> </dl>                                                                                                                                                               |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




