---
description: Возвращает адрес функции обратного вызова при сбое загрузки для указанной библиотеки DLL и процесса.
ms.assetid: db1d34cb-800a-4984-b4a3-d1ce1c6ee86c
title: Функция Делайлоадфаилурехук
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DelayLoadFailureHook
api_type:
- DllExport
api_location:
- kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-0.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
ms.openlocfilehash: f4986b70332a2581580d7e3b274e9d3cdcd96532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657216"
---
# <a name="delayloadfailurehook-function"></a>Функция Делайлоадфаилурехук

Возвращает адрес функции обратного вызова при сбое загрузки для указанной библиотеки DLL и процесса.

## <a name="syntax"></a>Синтаксис


```C++
FARPROC WINAPI DelayLoadFailureHook(
  _In_ LPCSTR pszDllName,
  _In_ LPCSTR pszProcName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псздллнаме* \[ окне\]
</dt> <dd>

Имя библиотеки DLL.

</dd> <dt>

*псзпрокнаме* \[ окне\]
</dt> <dd>

Имя процесса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Адрес функции обратного вызова.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Библиотека<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перехватчики ошибки](https://msdn.microsoft.com/library/sfcfb0a3(v=VS.71).aspx)
</dt> </dl>

 

 




