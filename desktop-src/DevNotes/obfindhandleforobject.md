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
ms.openlocfilehash: 7ba87d05d4264f3bb160bae16053a338e38e2145
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895557"
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

## <a name="remarks"></a>Комментарии

Эта функция доступна в Ntoskrnl.exe и может вызываться только из режима ядра. Соответствующая библиотека импорта доступна в комплекте драйверов Windows (WDK).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Нтосп. h</dt> </dl>      |
| Библиотека<br/>                  | <dl> <dt>Ntoskrnl. lib</dt> </dl> |



 

 




