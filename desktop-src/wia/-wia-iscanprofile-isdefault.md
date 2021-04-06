---
description: Возвращает значение, указывающее, является ли профиль профилем сканирования по умолчанию для связанного устройства IWiaItem2.
ms.assetid: 32ca3b9f-6235-4eec-aa94-bf20f15a9a16
title: 'Метод Исканпрофиле:: Default (Сканпрофиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.IsDefault
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 245d36d3f6c907260e3e4858a5873309d2638530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991276"
---
# <a name="iscanprofileisdefault-method"></a>Метод Исканпрофиле:: Default

Возвращает значение, указывающее, является ли профиль профилем сканирования по умолчанию для связанного устройства [**IWiaItem2**](-wia-iwiaitem2.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsDefault(
  [out] BOOL *pbDefault
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбдефаулт* \[ заполняет\]
</dt> <dd>

Тип: **bool \** _

Указатель на _ * BOOL * *.

<dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**УСЛОВИЯ**


</dt> <dd>

По умолчанию используется профиль.

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**ISFALSE**


</dt> <dd>

Профиль не является значением по умолчанию.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

*пбдефаулт* имеет **значение true** , если профиль содержит `<Default>` элемент. **Значение false** , если такой элемент отсутствует. Элемент не имеет значения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Сканпрофиле. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Сканпрофилес. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**исканпрофиле**](-wia-iscanprofile.md)
</dt> <dt>

[Схема профиля сканирования](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




