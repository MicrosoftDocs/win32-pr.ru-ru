---
description: Указывает, что Поиск завершен.
title: 'Метод Ишеллфолдерсеарчаблекаллбакк:: Руненд'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback.RunEnd
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91700764-6cdf-488d-adc0-e34d9b4cb71d
ms.openlocfilehash: 077ed97ad05ae3b12f3d00f695b15844a7b9ba05d693035b5ca8036b1d8da283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220370"
---
# <a name="ishellfoldersearchablecallbackrunend-method"></a>Метод Ишеллфолдерсеарчаблекаллбакк:: Руненд

Указывает, что Поиск завершен.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RunEnd(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двресервед* \[ окне\]
</dt> <dd>

Тип: **DWORD**

Зарезервировано. Должен иметь значение 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




