---
title: Имстскаксевентс, метод OnWarning
description: Вызывается, когда клиентский элемент управления обнаруживает неустранимое условие ошибки.
ms.assetid: af43d3aa-0ae8-4721-b85d-bb043b20dc40
ms.tgt_platform: multiple
keywords:
- Метод OnWarning службы удаленных рабочих столов
- Метод OnWarning службы удаленных рабочих столов, интерфейс Имстскаксевентс
- Интерфейс Имстскаксевентс службы удаленных рабочих столов, метод OnWarning
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnWarning
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aadc7013f34c93406f93841896a9041bbb1b7cfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802711"
---
# <a name="imstscaxeventsonwarning-method"></a>Метод Имстскаксевентс:: OnWarning

Вызывается, когда клиентский элемент управления обнаруживает неустранимое условие ошибки.

## <a name="syntax"></a>Синтаксис


```C++
void OnWarning(
  [in] long warningCode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*варнингкоде* \[ окне\]
</dt> <dd>

Код ошибки.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Кэш точечных рисунков поврежден.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имстскаксевентс**](imstscaxevents-interface.md)
</dt> </dl>

 

 





