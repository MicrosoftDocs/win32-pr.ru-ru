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
# <a name="ishellfoldersearchablecallback-interface"></a><span data-ttu-id="389d1-103">Интерфейс Ишеллфолдерсеарчаблекаллбакк</span><span class="sxs-lookup"><span data-stu-id="389d1-103">IShellFolderSearchableCallback interface</span></span>

<span data-ttu-id="389d1-104">Предоставляет подпрограммы обратного вызова для отслеживания процесса поиска.</span><span class="sxs-lookup"><span data-stu-id="389d1-104">Exposes callback routines to monitor the search process.</span></span>

## <a name="members"></a><span data-ttu-id="389d1-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="389d1-105">Members</span></span>

<span data-ttu-id="389d1-106">Интерфейс **ишеллфолдерсеарчаблекаллбакк** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="389d1-106">The **IShellFolderSearchableCallback** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="389d1-107">**Ишеллфолдерсеарчаблекаллбакк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="389d1-107">**IShellFolderSearchableCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="389d1-108">Методы</span><span class="sxs-lookup"><span data-stu-id="389d1-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="389d1-109">Методы</span><span class="sxs-lookup"><span data-stu-id="389d1-109">Methods</span></span>

<span data-ttu-id="389d1-110">Интерфейс **ишеллфолдерсеарчаблекаллбакк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="389d1-110">The **IShellFolderSearchableCallback** interface has these methods.</span></span>



| <span data-ttu-id="389d1-111">Метод</span><span class="sxs-lookup"><span data-stu-id="389d1-111">Method</span></span>                                                      | <span data-ttu-id="389d1-112">Описание</span><span class="sxs-lookup"><span data-stu-id="389d1-112">Description</span></span>                                      |
|:------------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="389d1-113">**рунбегин**</span><span class="sxs-lookup"><span data-stu-id="389d1-113">**RunBegin**</span></span>](ishellfoldersearchablecallback-runbegin.md) | <span data-ttu-id="389d1-114">Указывает, что был запущен Поиск.</span><span class="sxs-lookup"><span data-stu-id="389d1-114">Indicates that a search was started.</span></span><br/>  |
| [<span data-ttu-id="389d1-115">**руненд**</span><span class="sxs-lookup"><span data-stu-id="389d1-115">**RunEnd**</span></span>](ishellfoldersearchablecallback-runend.md)     | <span data-ttu-id="389d1-116">Указывает, что Поиск завершен.</span><span class="sxs-lookup"><span data-stu-id="389d1-116">Indicates that a search has finished.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="389d1-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="389d1-117">Remarks</span></span>

<span data-ttu-id="389d1-118">Этот интерфейс не определен ни в одном из файлов общедоступного заголовка.</span><span class="sxs-lookup"><span data-stu-id="389d1-118">This interface is not defined in any public header files.</span></span> <span data-ttu-id="389d1-119">Если вы решили реализовать этот интерфейс, можно использовать следующий код C/C++ для объявления своих методов.</span><span class="sxs-lookup"><span data-stu-id="389d1-119">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="389d1-120">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="389d1-120">Requirements</span></span>



| <span data-ttu-id="389d1-121">Требование</span><span class="sxs-lookup"><span data-stu-id="389d1-121">Requirement</span></span> | <span data-ttu-id="389d1-122">Значение</span><span class="sxs-lookup"><span data-stu-id="389d1-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="389d1-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="389d1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="389d1-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="389d1-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="389d1-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="389d1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="389d1-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="389d1-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="389d1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="389d1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="389d1-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="389d1-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
