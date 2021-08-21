---
title: Имстскаксевентс Онфаталеррор, метод
description: Вызывается, когда клиентский элемент управления обнаруживает неустранимую ошибку.
ms.assetid: 13a5eb2e-d847-4561-b30b-3f23a0579b4d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онфаталеррор
- Службы удаленных рабочих столов метода Онфаталеррор, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онфаталеррор
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFatalError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a10315eca4fcbf96edf123699614d29a2c0b8974f563c52148b5de75310fc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000684"
---
# <a name="imstscaxeventsonfatalerror-method"></a>Метод Имстскаксевентс:: Онфаталеррор

Вызывается, когда клиентский элемент управления обнаруживает неустранимую ошибку.

## <a name="syntax"></a>Синтаксис


```C++
void OnFatalError(
  [in] long errorCode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*код ошибки* \[ окне\]
</dt> <dd>

Указывает код ошибки.

<dt>

<span id="0"></span>

<span id="0"></span>**0,0**


</dt> <dd>

Произошла неизвестная ошибка.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Код внутренней ошибки 1.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Произошла ошибка нехватки памяти.

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3-5**


</dt> <dd>

Произошла ошибка при создании окна.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Код внутренней ошибки 2.

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5.0**


</dt> <dd>

Код внутренней ошибки 3. Это недопустимое состояние.

</dd> <dt>

<span id="6"></span>

<span id="6"></span>**1-6**


</dt> <dd>

Код внутренней ошибки 4.

</dd> <dt>

<span id="7"></span>

<span id="7"></span>**7**


</dt> <dd>

Во время подключения клиента произошла неустранимая ошибка.

</dd> <dt>

<span id="100"></span>

<span id="100"></span>**100**


</dt> <dd>

Ошибка инициализации Winsock.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

В ответ на это событие контейнер отображает сообщение об ошибке и завершает работу.

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>См. также

<dl> <dt>

[**имстскаксевентс**](imstscaxevents-interface.md)
</dt> </dl>

 

 





