---
description: Возвращает пользовательский значок устройства.
ms.assetid: 27763f39-80d8-4862-b045-e49c6e824c28
title: 'Метод Ивиауиекстенсион:: Жетдевицеикон (Виадевд. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 36b61a25de1acb9b84ce68dc897514e0d4612a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145388"
---
# <a name="iwiauiextensiongetdeviceicon-method"></a>Метод Ивиауиекстенсион:: Жетдевицеикон

Возвращает пользовательский значок устройства.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрдевицеид* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Указывает идентификатор устройства WIA, для которого должен быть получен значок.

</dd> <dt>

*фикон* \[ заполняет\]
</dt> <dd>

Тип: **Хикон \** _

Указывает на место в памяти, которое будет принимать маркер для значка устройства.

</dd> <dt>

_nSize * \[ в\]
</dt> <dd>

Тип: **ulong**

Задает требуемый размер значка в пикселях. Предполагается, что значок является квадратным, а Нсизе задает ширину и высоту запрошенного значка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Виадевд. h</dt> </dl> |



 

 




