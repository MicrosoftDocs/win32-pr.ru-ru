---
description: Приостанавливает процессы пакета, если они выполняются в данный момент.
ms.assetid: 83f44285-46ed-4968-b0af-7964dfacf602
title: 'Метод Ипаккажедебугсеттингс:: Suspend'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Suspend
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 385ddc856661090caec4345df6651605b67fe883
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809772"
---
# <a name="ipackagedebugsettingssuspend-method"></a>Метод Ипаккажедебугсеттингс:: Suspend

Приостанавливает процессы пакета, если они выполняются в данный момент.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Suspend(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*полноеимяпакета* \[ окне\]
</dt> <dd>

Тип: **лпквстр**

Полное имя пакета.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Этот метод может возвращать одно из этих значений.



| Код возврата                                                                                            | Описание                                      |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                   | Операция успешно выполнена.<br/>              |
| <dl> <dt>**E \_ недопустимое \_ STATECHANGE**</dt> </dl> | Процесс в данный момент не выполняется.<br/> |



 

## <a name="remarks"></a>Комментарии

Каждый процесс получает событие [**приостановки**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) . Он может быть полезен разработчикам для пошагового указания того, как приложения реагируют на это событие.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                          |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ипаккажедебугсеттингс**](/previous-versions//hh438393(v=vs.85))
</dt> </dl>

 

 
