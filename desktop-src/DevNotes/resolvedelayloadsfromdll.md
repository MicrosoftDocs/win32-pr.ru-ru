---
description: Пересылает работу в разрешении импортов с отложенной загрузкой из родительского двоичного файла в целевой двоичный файл.
ms.assetid: 65629d7b-36b0-426b-a20d-ec736b8461dc
title: Функция Ресолведелайлоадсфромдлл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadsFromDll
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: 894360a20456b73d0cfad19cd125405caf0c3624821aca21e3e107699d1cc372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571544"
---
# <a name="resolvedelayloadsfromdll-function"></a>Функция Ресолведелайлоадсфромдлл

Пересылает работу в разрешении импортов с отложенной загрузкой из родительского двоичного файла в целевой двоичный файл.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS WINAPI ResolveDelayLoadsFromDll(
  _In_       PVOID  ParentBase,
  _In_       LPCSTR TargetDllName,
  _Reserved_ ULONG  Flags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Парентбасе* \[ окне\]
</dt> <dd>

Базовый адрес модуля, который откладывает загрузку другого двоичного файла.

</dd> <dt>

*Таржетдллнаме* \[ окне\]
</dt> <dd>

Имя целевой библиотеки DLL.

</dd> <dt>

*Флаги* 
</dt> <dd>

Процессу значение должно быть равно 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Адрес дескриптора загрузки с задержкой, если он найден; в противном случае **значение NULL**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Библиотека<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Поддержка компоновщика для Delay-Loadedных библиотек DLL](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)
</dt> </dl>

 

 




