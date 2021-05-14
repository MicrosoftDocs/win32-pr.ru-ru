---
description: Возвращает имя представления по умолчанию. Вызовите Жетдисплайнамеоф, чтобы получить имена других представлений.
title: 'Метод Ишеллфолдервиевтипе:: Жетдефаултвиевнаме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetDefaultViewName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 99229d13-40dc-4750-81a7-48a2f608b778
ms.openlocfilehash: 808f68093512e2da602d5e73775b47943b140a46
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842765"
---
# <a name="ishellfolderviewtypegetdefaultviewname-method"></a>Метод Ишеллфолдервиевтипе:: Жетдефаултвиевнаме

Возвращает имя представления по умолчанию. Вызовите [**жетдисплайнамеоф**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) , чтобы получить имена других представлений.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDefaultViewName(
  [in]  DWORD  uFlags,
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*уфлагс* \[ окне\]
</dt> <dd>

Тип: **DWORD**

Необязательные флаги; необходимо задать значение 0.

</dd> <dt>

*ппвсзнаме* \[ заполняет\]
</dt> <dd>

Тип: **LPWSTR \***

Адрес указателя строки, который получает имя представления по умолчанию. Память для строки выделяется с помощью [**шстрдуп**](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa).

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



 

 




