---
description: Возвращает все доступные идентификаторы свойств в профиле.
ms.assetid: 9ef2abdd-0b33-4be3-a124-7795f42d5e55
title: 'Метод Исканпрофиле:: Жеталлпропидс (Сканпрофиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetAllPropIDs
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 34cd00f626bea3b8f1350950f0d2012ce019068e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692528"
---
# <a name="iscanprofilegetallpropids-method"></a>Метод Исканпрофиле:: Жеталлпропидс

Возвращает все доступные идентификаторы свойств в профиле.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetAllPropIDs(
  [in, out] ULONG  *num,
  [out]     PROPID *ppid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*число* \[ в, out\]
</dt> <dd>

Тип: **ulong \** _

Количество запрошенных или возвращаемых идентификаторов свойств.

</dd> <dt>

_ppid * \[ out\]
</dt> <dd>

Тип: **PropID \** _

Указатель на массив идентификаторов свойств.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

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

 

 




