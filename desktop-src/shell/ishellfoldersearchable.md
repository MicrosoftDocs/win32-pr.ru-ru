---
description: Предоставляет методы, позволяющие расширению оболочки предоставлять пространство имен с возможностью поиска.
title: Интерфейс Ишеллфолдерсеарчабле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 359def5c-d7ad-46bd-bdda-30a7b3eea56c
ms.openlocfilehash: 249ec6e6f1d4cbe471a89b19138a5b7a235536e595c62bc6d4a655bf55eee8d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220397"
---
# <a name="ishellfoldersearchable-interface"></a>Интерфейс Ишеллфолдерсеарчабле

Предоставляет методы, позволяющие расширению оболочки предоставлять пространство имен с возможностью поиска.

## <a name="members"></a>Элементы

Интерфейс **ишеллфолдерсеарчабле** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Ишеллфолдерсеарчабле** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ишеллфолдерсеарчабле** содержит следующие методы.



| Метод                                                                | Описание                                                               |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**канцеласинксеарч**](ishellfoldersearchable-cancelasyncsearch.md) | Начинает процесс отмены ожидающего асинхронного поиска.<br/> |
| [**FindString**](ishellfoldersearchable-findstring.md)               | Начинает поиск указанной строки поиска.<br/>                 |
| [**инвалидатесеарч**](ishellfoldersearchable-invalidatesearch.md)   | Делает это ПИДЛ недействительной частью папки оболочки.<br/>        |



 

## <a name="remarks"></a>Remarks

Этот интерфейс не определен ни в одном из файлов общедоступного заголовка. Если вы решили реализовать этот интерфейс, можно использовать следующий код C/C++ для объявления своих методов.


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchable
DECLARE_INTERFACE_IID_(IShellFolderSearchable, IUnknown, "4E1AE66C-204B-11d2-8DB3-0000F87A556C")
{
    // *** IUnknown methods ***
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void **ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // *** IShellFolderSearchable methods ***

    // FindString -
    //  The returned Shell folder's enumerator will have any
    //   search hits for the given search string.
    //  punkOnAsyncSearch will be QI'd for IShellFolderSearchableCallback
    STDMETHOD(FindString)(THIS_ LPCWSTR pwszTarget, __inout_opt DWORD *pdwFlags,
                          __in_opt IUnknown *punkOnAsyncSearch, __out LPITEMIDLIST *ppidlOut)   PURE;
    // CancelAsyncSearch -
    //   Begins the process of canceling any pending
    //    asynchronous search from this pidl.
    //    When the search is actually canceled, RunEnd will be called
    //   Returns: S_OK => cancelling, S_FALSE => not running
    STDMETHOD(CancelAsyncSearch) (THIS_ LPCITEMIDLIST pidlSearch, __inout_opt DWORD *pdwFlags) PURE;

    // InvalidateSearch -
    //   Makes this pidl no longer a valid portion of the Shell folder
    //    Also does some cleanup of any databases used in the search and
    //    will cause the eventual release of the callback
    //   May cause async search to be canceled
    STDMETHOD(InvalidateSearch)  (THIS_ LPCITEMIDLIST pidlSearch, __inout_opt DWORD *pdwFlags) PURE;
};
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
