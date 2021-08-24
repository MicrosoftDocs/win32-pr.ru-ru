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
ms.openlocfilehash: cb5c6e324e657962a4a0bbbfa64cb45fefa7d37a3ca5ce21cd25e072fc1a6594
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119223374"
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



 

 




