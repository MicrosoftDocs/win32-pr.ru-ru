---
description: Функция Експертсубмитевент указывает, что существует условие события и предоставляет структуру данных, описывающую условие.
ms.assetid: 2339b530-427b-4028-aef6-c2cdd1353f77
title: Функция Експертсубмитевент (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertSubmitEvent
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b6ce73d378e4d8432459a23a76b30ebf4d558a5f82ec230e6841eeeb621aed13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744224"
---
# <a name="expertsubmitevent-function"></a>Функция Експертсубмитевент

Функция **експертсубмитевент** указывает, что существует условие события и предоставляет структуру данных, описывающую условие.

## <a name="syntax"></a>Синтаксис


```C++
DWORD WINAPI ExpertSubmitEvent(
  _In_ HEXPERTKEY   hExpertKey,
  _In_ PNMEVENTDATA pExpertEvent
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хексперткэй* \[ окне\]
</dt> <dd>

Уникальный идентификатор эксперта. Сетевой монитор передает *хексперткэй* эксперту при вызове функции [Run](run.md) .

</dd> <dt>

*пекспертевент* \[ окне\]
</dt> <dd>

Указатель на структуру **нмевентдата** , описывающую условие события.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.

Если функция завершается неудачно, возвращаемое значение указывает причину сбоя. Если возвращаемое значение — НМЕРР \_ \_ , то эксперт немедленно очищается и возвращает результат.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




