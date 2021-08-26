---
description: Извлекает маркер объекта для указанного объекта, связанного с указанным процессом.
ms.assetid: c7b371c3-02c0-4137-ad9d-dd07a74fe2a5
title: Функция Обфиндхандлефоробжект (Нтосп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObFindHandleForObject
api_type:
- LibDef
api_location:
- Ntoskrnl.lib
- Ntoskrnl.dll
ms.openlocfilehash: 481def34e3e8656205eefe96058fe3c7558d2c898c7e05ddc78f9a67435c507e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984154"
---
# <a name="obfindhandleforobject-function"></a>Функция Обфиндхандлефоробжект

\[Эта функция устарела и может быть изменена или недоступна в будущих версиях Windows. Старайтесь не использовать эту функцию.\]

Извлекает маркер объекта для указанного объекта, связанного с указанным процессом.

## <a name="syntax"></a>Синтаксис


```C++
BOOLEAN WINAPI ObFindHandleForObject(
  _In_     PEPROCESS Process,
  _In_     PVOID     Object,
  _In_opt_ PVOID     Reserved1,
  _In_opt_ PVOID     Reserved2,
  _Out_    PHANDLE   Handle
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Обработка* \[ окне\]
</dt> <dd>

Процесс. Этот маркер возвращается функцией **иожеткуррентпроцесс** или **псжеткуррентпроцесс** .

</dd> <dt>

*Объект* \[ окне\]
</dt> <dd>

Указатель на объект.

</dd> <dt>

*Reserved1* \[ в необязательное\]
</dt> <dd>

Зарезервировано.

</dd> <dt>

*Reserved2* \[ в необязательное\]
</dt> <dd>

Зарезервировано.

</dd> <dt>

*Обработчик* \[ заполняет\]
</dt> <dd>

Объектный обработчик.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **значение true** , если найдено совпадение, и **false** в противном случае.

## <a name="remarks"></a>Remarks

Эта функция доступна в Ntoskrnl.exe и может вызываться только из режима ядра. соответствующая библиотека импорта доступна в комплекте Windows Driver Kit (WDK).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Нтосп. h</dt> </dl>      |
| Библиотека<br/>                  | <dl> <dt>Ntoskrnl. lib</dt> </dl> |



 

 




