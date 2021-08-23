---
description: Находит целевую функцию указанного импорта и заменяет указатель функции в преобразователе импорта на целевой объект реализации функции.
ms.assetid: 4ab79b7c-81d1-40bf-a76b-217d93567e40
title: Функция Ресолведелайлоадедапи
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadedAPI
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: 359de5c52417f09c35e2fc994e36f0efd054f2a18dc3063be71dc12d588c60e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571554"
---
# <a name="resolvedelayloadedapi-function"></a>Функция Ресолведелайлоадедапи

Находит целевую функцию указанного импорта и заменяет указатель функции в преобразователе импорта на целевой объект реализации функции.

## <a name="syntax"></a>Синтаксис


```C++
PVOID WINAPI ResolveDelayLoadedAPI(
  _In_       PVOID                             ParentModuleBase,
  _In_       PCIMAGE_DELAYLOAD_DESCRIPTOR      DelayloadDescriptor,
  _In_opt_   PDELAYLOAD_FAILURE_DLL_CALLBACK   FailureDllHook,
  _In_opt_   PDELAYLOAD_FAILURE_SYSTEM_ROUTINE FailureSystemHook,
  _Out_      PIMAGE_THUNK_DATA                 ThunkAddress,
  _Reserved_ ULONG                             Flags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Парентмодулебасе* \[ окне\]
</dt> <dd>

Адрес основания модуля, в котором импортируется функция с отложенной загрузкой.

</dd> <dt>

*Делайлоаддескриптор* \[ окне\]
</dt> <dd>

Дескриптор загружаемого модуля.

</dd> <dt>

*Фаилуредллхук* \[ в необязательное\]
</dt> <dd>

Адрес ловушки сбоя. См. [**делайлоадфаилурехук**](delayloadfailurehook.md).

</dd> <dt>

*Фаилуресистемхук* \[ в необязательное\]
</dt> <dd>

Адрес обработчика ошибок системы.

</dd> <dt>

*Сункаддресс* \[ заполняет\]
</dt> <dd>

Данные преобразователя для целевой функции. Используется для поиска конкретной записи таблицы имен функции.

</dd> <dt>

*Флаги* 
</dt> <dd>

Процессу значение должно быть равно 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Адрес импорта или заглушка сбоя для него.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Библиотека<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Поддержка компоновщика для Delay-Loadedных библиотек DLL](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)
</dt> </dl>

 

 




