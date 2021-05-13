---
description: Предоставляет методы, позволяющие папке оболочки поддерживать различные представления содержимого (различные иерархические макеты данных).
title: Интерфейс Ишеллфолдервиевтипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9b597f6b-ef27-4fa1-ad00-e131dbd979e7
ms.openlocfilehash: f3ccb4073d59e0ebe9b840bd6f8f592f463e1e46
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842695"
---
# <a name="ishellfolderviewtype-interface"></a><span data-ttu-id="139e6-103">Интерфейс Ишеллфолдервиевтипе</span><span class="sxs-lookup"><span data-stu-id="139e6-103">IShellFolderViewType interface</span></span>

<span data-ttu-id="139e6-104">Предоставляет методы, позволяющие папке оболочки поддерживать различные представления содержимого (различные иерархические макеты данных).</span><span class="sxs-lookup"><span data-stu-id="139e6-104">Exposes methods that enable a Shell folder to support different views on its content (different hierarchical layouts of its data).</span></span>

## <a name="members"></a><span data-ttu-id="139e6-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="139e6-105">Members</span></span>

<span data-ttu-id="139e6-106">Интерфейс **ишеллфолдервиевтипе** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="139e6-106">The **IShellFolderViewType** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="139e6-107">**Ишеллфолдервиевтипе** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="139e6-107">**IShellFolderViewType** also has these types of members:</span></span>

-   [<span data-ttu-id="139e6-108">Методы</span><span class="sxs-lookup"><span data-stu-id="139e6-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="139e6-109">Методы</span><span class="sxs-lookup"><span data-stu-id="139e6-109">Methods</span></span>

<span data-ttu-id="139e6-110">Интерфейс **ишеллфолдервиевтипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="139e6-110">The **IShellFolderViewType** interface has these methods.</span></span>



| <span data-ttu-id="139e6-111">Метод</span><span class="sxs-lookup"><span data-stu-id="139e6-111">Method</span></span>                                                                      | <span data-ttu-id="139e6-112">Описание</span><span class="sxs-lookup"><span data-stu-id="139e6-112">Description</span></span>                                                                                                                                                          |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="139e6-113">**енумвиевс**</span><span class="sxs-lookup"><span data-stu-id="139e6-113">**EnumViews**</span></span>](ishellfolderviewtype-enumviews.md)                         | <span data-ttu-id="139e6-114">Получает перечислитель, возвращающий один ПИДЛ для каждого расширенного представления.</span><span class="sxs-lookup"><span data-stu-id="139e6-114">Retrieves an enumerator that will return one PIDL for every extended view.</span></span><br/>                                                                                |
| [<span data-ttu-id="139e6-115">**жетдефаултвиевнаме**</span><span class="sxs-lookup"><span data-stu-id="139e6-115">**GetDefaultViewName**</span></span>](ishellfolderviewtype-getdefaultviewname.md)       | <span data-ttu-id="139e6-116">Возвращает имя представления по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="139e6-116">Gets the name of the default view.</span></span> <span data-ttu-id="139e6-117">Вызовите метод [**ишеллфолдер:: жетдисплайнамеоф**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) , чтобы получить имена других представлений.</span><span class="sxs-lookup"><span data-stu-id="139e6-117">Call [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to retrieve the names of the other views.</span></span><br/> |
| [<span data-ttu-id="139e6-118">**жетвиевтипепропертиес**</span><span class="sxs-lookup"><span data-stu-id="139e6-118">**GetViewTypeProperties**</span></span>](ishellfolderviewtype-getviewtypeproperties.md) | <span data-ttu-id="139e6-119">Возвращает свойства представления.</span><span class="sxs-lookup"><span data-stu-id="139e6-119">Gets the properties of the view.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="139e6-120">**транслатевиевпидл**</span><span class="sxs-lookup"><span data-stu-id="139e6-120">**TranslateViewPidl**</span></span>](ishellfolderviewtype-translateviewpidl.md)         | <span data-ttu-id="139e6-121">Восстанавливает ПИДЛ из одного иерархического представления папки оболочки в другое представление.</span><span class="sxs-lookup"><span data-stu-id="139e6-121">Reconstructs a PIDL from one hierarchical representation of the Shell folder into a different representation.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="139e6-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="139e6-122">Remarks</span></span>

<span data-ttu-id="139e6-123">Этот перечислитель возвращает PIDL, которые являются специальными скрытыми папками на верхнем уровне папки оболочки, которые в противном случае не перечисляются.</span><span class="sxs-lookup"><span data-stu-id="139e6-123">This enumerator returns PIDLs that are special hidden folders at the top level of the Shell folder, which are not otherwise enumerated.</span></span> <span data-ttu-id="139e6-124">Представление по умолчанию — это одна из папок оболочки, отображаемая в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="139e6-124">The default view is the one the Shell folder displays normally.</span></span>

<span data-ttu-id="139e6-125">Этот интерфейс не определен ни в одном из файлов общедоступного заголовка.</span><span class="sxs-lookup"><span data-stu-id="139e6-125">This interface is not defined in any public header file.</span></span> <span data-ttu-id="139e6-126">Если вы решили реализовать этот интерфейс, можно использовать следующий код C/C++ для объявления своих методов.</span><span class="sxs-lookup"><span data-stu-id="139e6-126">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


```
#undef  INTERFACE
#define INTERFACE   IShellFolderViewType
DECLARE_INTERFACE_IID_(IShellFolderViewType, IUnknown, "49422C1E-1C03-11d2-8DAB-0000F87A556C")
{
    // *** IUnknown methods ***
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void **ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // *** IShellFolderViewType Methods ***

    // EnumViews:
    //   Returns an enumerator which will give out one pidl for every extended view.
    STDMETHOD(EnumViews)(THIS_ ULONG grfFlags, __out IEnumIDList **ppenum) PURE;

    // GetDefaultViewName:
    //   Returns the name of the default view.  The names of the other views
    //   can be retrieved by calling GetDisplayNameOf.
    STDMETHOD(GetDefaultViewName)(THIS_ DWORD  uFlags, __out LPWSTR *ppwszName) PURE;
    STDMETHOD(GetViewTypeProperties)(THIS_ PCUITEMID_CHILD pidl, __out DWORD *pdwFlags)  PURE;

    // TranslateViewPidl:
    //   Attempts to take a pidl represented in one hierarchical representation of
    //   the Shell folder, and find it in a different representation.
    //   pidl should be relative to the root folder.
    //   Remember to ILFree ppidlOut
    STDMETHOD(TranslateViewPidl)(THIS_ PCUIDLIST_RELATIVE pidl, PCUIDLIST_RELATIVE pidlView,
              __out PIDLIST_RELATIVE *ppidlOut) PURE;
};

#define SFVTFLAG_NOTIFY_CREATE  0x00000001
#define SFVTFLAG_NOTIFY_RESORT  0x00000002
```



## <a name="requirements"></a><span data-ttu-id="139e6-127">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="139e6-127">Requirements</span></span>



| <span data-ttu-id="139e6-128">Требование</span><span class="sxs-lookup"><span data-stu-id="139e6-128">Requirement</span></span> | <span data-ttu-id="139e6-129">Значение</span><span class="sxs-lookup"><span data-stu-id="139e6-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="139e6-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="139e6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="139e6-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="139e6-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="139e6-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="139e6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="139e6-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="139e6-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="139e6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="139e6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="139e6-135"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="139e6-135"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
