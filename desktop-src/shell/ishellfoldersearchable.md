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
ms.openlocfilehash: 6daa00e6821833d783aefa95be23b7b8de769907
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842835"
---
# <a name="ishellfoldersearchable-interface"></a><span data-ttu-id="11175-103">Интерфейс Ишеллфолдерсеарчабле</span><span class="sxs-lookup"><span data-stu-id="11175-103">IShellFolderSearchable interface</span></span>

<span data-ttu-id="11175-104">Предоставляет методы, позволяющие расширению оболочки предоставлять пространство имен с возможностью поиска.</span><span class="sxs-lookup"><span data-stu-id="11175-104">Exposes methods that allow a Shell extension to provide a searchable namespace.</span></span>

## <a name="members"></a><span data-ttu-id="11175-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="11175-105">Members</span></span>

<span data-ttu-id="11175-106">Интерфейс **ишеллфолдерсеарчабле** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="11175-106">The **IShellFolderSearchable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="11175-107">**Ишеллфолдерсеарчабле** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="11175-107">**IShellFolderSearchable** also has these types of members:</span></span>

-   [<span data-ttu-id="11175-108">Методы</span><span class="sxs-lookup"><span data-stu-id="11175-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="11175-109">Методы</span><span class="sxs-lookup"><span data-stu-id="11175-109">Methods</span></span>

<span data-ttu-id="11175-110">Интерфейс **ишеллфолдерсеарчабле** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="11175-110">The **IShellFolderSearchable** interface has these methods.</span></span>



| <span data-ttu-id="11175-111">Метод</span><span class="sxs-lookup"><span data-stu-id="11175-111">Method</span></span>                                                                | <span data-ttu-id="11175-112">Описание</span><span class="sxs-lookup"><span data-stu-id="11175-112">Description</span></span>                                                               |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="11175-113">**канцеласинксеарч**</span><span class="sxs-lookup"><span data-stu-id="11175-113">**CancelAsyncSearch**</span></span>](ishellfoldersearchable-cancelasyncsearch.md) | <span data-ttu-id="11175-114">Начинает процесс отмены ожидающего асинхронного поиска.</span><span class="sxs-lookup"><span data-stu-id="11175-114">Begins the process of canceling a pending asynchronous search.</span></span><br/> |
| [<span data-ttu-id="11175-115">**FindString**</span><span class="sxs-lookup"><span data-stu-id="11175-115">**FindString**</span></span>](ishellfoldersearchable-findstring.md)               | <span data-ttu-id="11175-116">Начинает поиск указанной строки поиска.</span><span class="sxs-lookup"><span data-stu-id="11175-116">Begins a search for a specified search string.</span></span><br/>                 |
| [<span data-ttu-id="11175-117">**инвалидатесеарч**</span><span class="sxs-lookup"><span data-stu-id="11175-117">**InvalidateSearch**</span></span>](ishellfoldersearchable-invalidatesearch.md)   | <span data-ttu-id="11175-118">Делает это ПИДЛ недействительной частью папки оболочки.</span><span class="sxs-lookup"><span data-stu-id="11175-118">Makes this PIDL an invalid portion of the Shell folder.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="11175-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="11175-119">Remarks</span></span>

<span data-ttu-id="11175-120">Этот интерфейс не определен ни в одном из файлов общедоступного заголовка.</span><span class="sxs-lookup"><span data-stu-id="11175-120">This interface is not defined in any public header files.</span></span> <span data-ttu-id="11175-121">Если вы решили реализовать этот интерфейс, можно использовать следующий код C/C++ для объявления своих методов.</span><span class="sxs-lookup"><span data-stu-id="11175-121">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="11175-122">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="11175-122">Requirements</span></span>



| <span data-ttu-id="11175-123">Требование</span><span class="sxs-lookup"><span data-stu-id="11175-123">Requirement</span></span> | <span data-ttu-id="11175-124">Значение</span><span class="sxs-lookup"><span data-stu-id="11175-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11175-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11175-125">Minimum supported client</span></span><br/> | <span data-ttu-id="11175-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="11175-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="11175-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11175-127">Minimum supported server</span></span><br/> | <span data-ttu-id="11175-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="11175-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="11175-129">DLL</span><span class="sxs-lookup"><span data-stu-id="11175-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11175-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11175-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
