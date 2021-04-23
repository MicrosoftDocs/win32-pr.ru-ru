---
description: Предоставляет доступ ко всем планшетам, подключенным к компьютеру.
ms.assetid: d0fd9a6f-93fe-43d6-97fd-fee45854dfa1
title: Интерфейс Итаблетманажер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 3400d98a832819d1edd640cd78586f1cfb06bdee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081542"
---
# <a name="itabletmanager-interface"></a><span data-ttu-id="8ebff-103">Интерфейс Итаблетманажер</span><span class="sxs-lookup"><span data-stu-id="8ebff-103">ITabletManager interface</span></span>

<span data-ttu-id="8ebff-104">Предоставляет доступ ко всем планшетам, подключенным к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="8ebff-104">Provides access to all of the tablets attached to the computer.</span></span>

## <a name="members"></a><span data-ttu-id="8ebff-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="8ebff-105">Members</span></span>

<span data-ttu-id="8ebff-106">Интерфейс **итаблетманажер** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8ebff-106">The **ITabletManager** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8ebff-107">**Итаблетманажер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8ebff-107">**ITabletManager** also has these types of members:</span></span>

-   [<span data-ttu-id="8ebff-108">Методы</span><span class="sxs-lookup"><span data-stu-id="8ebff-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8ebff-109">Методы</span><span class="sxs-lookup"><span data-stu-id="8ebff-109">Methods</span></span>

<span data-ttu-id="8ebff-110">Интерфейс **итаблетманажер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8ebff-110">The **ITabletManager** interface has these methods.</span></span>



| <span data-ttu-id="8ebff-111">Метод</span><span class="sxs-lookup"><span data-stu-id="8ebff-111">Method</span></span>                                                  | <span data-ttu-id="8ebff-112">Описание</span><span class="sxs-lookup"><span data-stu-id="8ebff-112">Description</span></span>                                                        |
|:--------------------------------------------------------|:-------------------------------------------------------------------|
| <span data-ttu-id="8ebff-113">[**Подтаблица**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8ebff-113">[**GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85))</span></span>           | <span data-ttu-id="8ebff-114">Извлекает указанный объект планшета.</span><span class="sxs-lookup"><span data-stu-id="8ebff-114">Retrieves the specified tablet object.</span></span><br/>                  |
| [<span data-ttu-id="8ebff-115">**жеттаблеткаунт**</span><span class="sxs-lookup"><span data-stu-id="8ebff-115">**GetTabletCount**</span></span>](itabletmanager-gettabletcount.md) | <span data-ttu-id="8ebff-116">Возвращает число планшетов, подключенных к системе.</span><span class="sxs-lookup"><span data-stu-id="8ebff-116">Retrieves the number of tablets attached to the system.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8ebff-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ebff-117">Remarks</span></span>

<span data-ttu-id="8ebff-118">Разработчики не должны использовать этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="8ebff-118">Developers should not use this interface.</span></span>

<span data-ttu-id="8ebff-119">В следующем коде показано, как реализуется интерфейс **итаблетманажер** .</span><span class="sxs-lookup"><span data-stu-id="8ebff-119">The following code shows how the **ITabletManager** interface is implemented.</span></span>

``` syntax
[
    object,
    uuid(764DE8AA-1867-47C1-8F6A-122445ABD89A),
    pointer_default(unique)
]
interface ITabletManager : IUnknown
{
    HRESULT GetDefaultTablet(
        [out] ITablet **ppTablet);

    HRESULT GetTabletCount(
        [out] ULONG *pcTablets);

    HRESULT GetTablet(
        [in] ULONG iTablet,
        [out] ITablet **ppTablet);

    HRESULT GetTabletContextById(
        [in] TABLET_CONTEXT_ID tcid,
        [out] ITabletContext **ppContext);

    HRESULT GetCursorById(
        [in] CURSOR_ID cid,
        [out] ITabletCursor **ppCursor);
};
        
        
```

<span data-ttu-id="8ebff-120">Вызовите [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) с идентификатором класса CLSID \_ таблетманажерс, а затем вызовите [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) , чтобы получить указатель на **интерфейс итаблетманажер**.</span><span class="sxs-lookup"><span data-stu-id="8ebff-120">Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) with a class ID of CLSID\_TabletManagerS, and then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get a pointer to the **ITabletManager Interface**.</span></span> <span data-ttu-id="8ebff-121">\_Идентификатор GUID ТАБЛЕТМАНАЖЕРС CLSID определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8ebff-121">The CLSID\_TabletManagerS GUID is defined as follows:</span></span>

``` syntax
#define CLSID_TabletManagerS uuid(A5B020FD-E04B-4e67-B65A-E7DEED25B2CF)
```

## <a name="requirements"></a><span data-ttu-id="8ebff-122">Требования</span><span class="sxs-lookup"><span data-stu-id="8ebff-122">Requirements</span></span>



| <span data-ttu-id="8ebff-123">Требование</span><span class="sxs-lookup"><span data-stu-id="8ebff-123">Requirement</span></span> | <span data-ttu-id="8ebff-124">Значение</span><span class="sxs-lookup"><span data-stu-id="8ebff-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ebff-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8ebff-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8ebff-126">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8ebff-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8ebff-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8ebff-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8ebff-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8ebff-128">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8ebff-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8ebff-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="8ebff-130"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8ebff-130"><dt>Wisptis.exe</dt></span></span> </dl> |



 

