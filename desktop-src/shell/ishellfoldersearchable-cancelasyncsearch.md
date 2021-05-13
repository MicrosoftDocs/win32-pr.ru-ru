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
ms.openlocfilehash: 3146fea4f6c8d8547c8c86096b434cbaea5b5926
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842995"
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

Тип: **DWORD \***

Флаги в настоящее время не определены; Задайте **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Возвращает \_ значение s ОК при отмене или \_ false, если поиск не выполняется.

## <a name="remarks"></a>Remarks

При фактическом отмене поиска будет вызван [**руненд**](ishellfoldersearchablecallback-runend.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




