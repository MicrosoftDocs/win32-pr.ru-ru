---
description: Начинает процесс отмены ожидающего асинхронного поиска.
title: 'Метод Ишеллфолдерсеарчабле:: Канцеласинксеарч'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.CancelAsyncSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5c920dca-fbca-48e1-9dce-38713cf1fcef
ms.openlocfilehash: e9e3231e8cc602a4e00b6ee79a25392717b6e68b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984637"
---
# <a name="ishellfoldersearchablecancelasyncsearch-method"></a>Метод Ишеллфолдерсеарчабле:: Канцеласинксеарч

Начинает процесс отмены ожидающего асинхронного поиска.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CancelAsyncSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пидлсеарч* \[ окне\]
</dt> <dd>

Тип: **лпЦитемидлист**

Указатель на [**итемидлист**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) для поиска.

</dd> <dt>

*пдвфлагс* \[ окне\]
</dt> <dd>

Введите: **DWORD \** _

Флаги в настоящее время не определены; Задайте значение _ * NULL * *.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Возвращает \_ значение s ОК при отмене или \_ false, если поиск не выполняется.

## <a name="remarks"></a>Примечания

При фактическом отмене поиска будет вызван [**руненд**](ishellfoldersearchablecallback-runend.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




