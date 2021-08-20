---
description: Отключает функции.
ms.assetid: 2ea2dcfb-84e6-4f83-9afd-c3050b53f37c
title: Функция Псетупсетглобалфлагс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupSetGlobalFlags
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: d28bb948d351b2b9ad54c7e2bdc8c8cbfde83f6f4ade42a0f90440eca28bfc05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955703"
---
# <a name="psetupsetglobalflags-function"></a>Функция Псетупсетглобалфлагс

\[эта функция недоступна в Windows Vista или Windows Server 2008.\]

Отключает функции.

## <a name="syntax"></a>Синтаксис


```C++
VOID pSetupSetGlobalFlags(
  _In_ DWORD Value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Значение* \[ окне\]
</dt> <dd>

Флаги, используемые для отключения пользовательского интерфейса или автоматического резервного копирования.



| Значение                                                                                                                                                                                                                                         | Значение                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PSPGF_NONINTERACTIVE"></span><span id="pspgf_noninteractive"></span><dl> <dt>**Пспгф \_ Неинтерактивный**</dt> <dt>0x004</dt> </dl> | Установите для отключения интерфейса пользователя.<br/>   |
| <span id="PSPGF_NO_BACKUP"></span><span id="pspgf_no_backup"></span><dl> <dt>**Пспгф \_ НЕТ \_ резервной копии**</dt> <dt>0x002</dt> </dl>               | Установите для отключения автоматической архивации.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
