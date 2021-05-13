---
description: Предоставляет подпрограммы обратного вызова для отслеживания процесса поиска.
title: Интерфейс Ишеллфолдерсеарчаблекаллбакк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3412a01b-d5ea-44e1-819c-f10f81fac391
ms.openlocfilehash: cf1a3b03eed2a15e82e1313875a4ab8584243190
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842785"
---
# <a name="ishellfoldersearchablecallback-interface"></a>Интерфейс Ишеллфолдерсеарчаблекаллбакк

Предоставляет подпрограммы обратного вызова для отслеживания процесса поиска.

## <a name="members"></a>Элементы

Интерфейс **ишеллфолдерсеарчаблекаллбакк** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Ишеллфолдерсеарчаблекаллбакк** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ишеллфолдерсеарчаблекаллбакк** содержит следующие методы.



| Метод                                                      | Описание                                      |
|:------------------------------------------------------------|:-------------------------------------------------|
| [**рунбегин**](ishellfoldersearchablecallback-runbegin.md) | Указывает, что был запущен Поиск.<br/>  |
| [**руненд**](ishellfoldersearchablecallback-runend.md)     | Указывает, что Поиск завершен.<br/> |



 

## <a name="remarks"></a>Remarks

Этот интерфейс не определен ни в одном из файлов общедоступного заголовка. Если вы решили реализовать этот интерфейс, можно использовать следующий код C/C++ для объявления своих методов.


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchableCallback
DECLARE_INTERFACE_IID_(IShellFolderSearchableCallback, IUnknown, "F98D8294-2BBC-11d2-8DBD-0000F87A556C")
{
    // *** IUnknown methods ***
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void **ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // *** IShellFolderSearchableCallback Methods ***

    STDMETHOD(RunBegin)(THIS_ DWORD dwReserved) PURE;
    STDMETHOD(RunEnd)(THIS_ DWORD dwReserved) PURE;
};
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
