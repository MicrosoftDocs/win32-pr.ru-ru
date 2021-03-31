---
description: Функция Експертжетстартупинфо извлекает сведения о конфигурации запуска эксперта.
ms.assetid: 15f080ed-50b7-40c6-b283-dbe416a2b0e9
title: Функция Експертжетстартупинфо (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetStartupInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f34ecc3d0c3eeb085d2a7c0f8c4cb0426663093c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423682"
---
# <a name="expertgetstartupinfo-function"></a>Функция Експертжетстартупинфо

Функция **експертжетстартупинфо** извлекает сведения о конфигурации запуска эксперта.

## <a name="syntax"></a>Синтаксис


```C++
DWORD WINAPI ExpertGetStartupInfo(
  _In_  HEXPERTKEY         hExpertKey,
  _Out_ PEXPERTSTARTUPINFO pExpertStartupInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хексперткэй* \[ окне\]
</dt> <dd>

Уникальный идентификатор эксперта. Сетевой монитор передает *хексперткэй* эксперту при вызове функции [Run](run.md) .

</dd> <dt>

*пекспертстартупинфо* \[ заполняет\]
</dt> <dd>

Указатель на структуру [експертстартупинфо](expertstartupinfo.md) , содержащую сведения о запуске.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.

Если функция завершается неудачно, возвращается значение НМЕРР.

## <a name="remarks"></a>Комментарии

Функция **експертжетстартупинфо** используется, если эксперт должен определить используемые сведения о запуске.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




