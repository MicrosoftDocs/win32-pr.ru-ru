---
description: Инициализирует необязательный Диспетчер компонентов.
ms.assetid: 9a7ddca6-a6c8-4d96-81bb-66158b83ab68
title: Функция ОЦинитиализе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcInitialize
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: 08e7ffd7f8ad6faa2b08f937627627b6e74bbc09505482c589023db5dae37677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826749"
---
# <a name="ocinitialize-function"></a>Функция ОЦинитиализе

Инициализирует необязательный Диспетчер компонентов.

## <a name="syntax"></a>Синтаксис


```C++
PVOID OcInitialize(
  _In_  POCM_CLIENT_CALLBACKS Callbacks,
  _In_  LPCTSTR               MasterOcInfName,
  _In_  UINT                  Flags,
  _Out_ PBOOL                 ShowError,
  _In_  PVOID                 Log
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Обратные вызовы* \[ окне\]
</dt> <dd>

Указатель на структуру [**\_ \_ обратных вызовов клиента OCM**](ocm-client-callbacks.md) , указывающий функции обратного вызова, которые используются диспетчером OC для выполнения различных задач.

</dd> <dt>

*МастероЦинфнаме* \[ окне\]
</dt> <dd>

Путь к главному файлу OC. INF.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Этот параметр может принимать одно или несколько следующих значений.

<dl> <dt>

<span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**ОЦинит \_ ФОРЦЕНЕВИНФ** (0x00000001)
</dt> <dt>

<span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**ОЦинит \_ КИЛЛСУБКОМПС** (0x00000002)
</dt> <dt>

<span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**ОЦинит \_ РУНКУИЕТ** (0x00000004)
</dt> <dt>

<span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**ОЦинит \_ ЛАНГУАЖЕАВАРЕ** (0x00000008)
</dt> </dl> </dd> <dt>

*ShowError* \[ заполняет\]
</dt> <dd>

Если функция завершается ошибкой, этот параметр указывает, следует ли отображать сообщение об ошибке.

</dd> <dt>

*Журнал* \[ окне\]
</dt> <dd>

Маркер журнала.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает значение контекста для диспетчера OC.

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>OcManage.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ обратные вызовы клиента OCM**](ocm-client-callbacks.md)
</dt> <dt>

[**октерминате**](octerminate.md)
</dt> </dl>

 

 
