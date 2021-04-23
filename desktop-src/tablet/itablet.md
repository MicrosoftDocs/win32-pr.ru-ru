---
description: Представляет планшет, подключенный к компьютеру.
ms.assetid: 31e11f7d-5610-4c49-9203-2dc322fbef95
title: Интерфейс Итаблет
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 76fa7baea2713e5a2e5eaae562b6dac29e002fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719589"
---
# <a name="itablet-interface"></a><span data-ttu-id="47ecf-103">Интерфейс Итаблет</span><span class="sxs-lookup"><span data-stu-id="47ecf-103">ITablet interface</span></span>

<span data-ttu-id="47ecf-104">Представляет планшет, подключенный к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="47ecf-104">Represents a tablet attached to the computer.</span></span>

## <a name="members"></a><span data-ttu-id="47ecf-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="47ecf-105">Members</span></span>

<span data-ttu-id="47ecf-106">Интерфейс **итаблет** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="47ecf-106">The **ITablet** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="47ecf-107">**Итаблет** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="47ecf-107">**ITablet** also has these types of members:</span></span>

-   [<span data-ttu-id="47ecf-108">Методы</span><span class="sxs-lookup"><span data-stu-id="47ecf-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="47ecf-109">Методы</span><span class="sxs-lookup"><span data-stu-id="47ecf-109">Methods</span></span>

<span data-ttu-id="47ecf-110">Интерфейс **итаблет** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="47ecf-110">The **ITablet** interface has these methods.</span></span>



| <span data-ttu-id="47ecf-111">Метод</span><span class="sxs-lookup"><span data-stu-id="47ecf-111">Method</span></span>                                                                 | <span data-ttu-id="47ecf-112">Описание</span><span class="sxs-lookup"><span data-stu-id="47ecf-112">Description</span></span>                                                                           |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="47ecf-113">**CreateContext**</span><span class="sxs-lookup"><span data-stu-id="47ecf-113">**CreateContext**</span></span>](itablet-createcontext.md)                         | <span data-ttu-id="47ecf-114">Создает объект контекста, описывающий указанное устройство планшета.</span><span class="sxs-lookup"><span data-stu-id="47ecf-114">Creates a context object that describes the specified tablet device.</span></span><br/>       |
| <span data-ttu-id="47ecf-115">[**Навести курсор**](/previous-versions/windows/desktop/legacy/aa373535(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="47ecf-115">[**GetCursor**](/previous-versions/windows/desktop/legacy/aa373535(v=vs.85))</span></span>                                 | <span data-ttu-id="47ecf-116">Извлекает указанный объект [**итаблеткурсор**](itabletcursor.md) .</span><span class="sxs-lookup"><span data-stu-id="47ecf-116">Retrieves the specified [**ITabletCursor**](itabletcursor.md) object.</span></span><br/>     |
| [<span data-ttu-id="47ecf-117">**жеткурсоркаунт**</span><span class="sxs-lookup"><span data-stu-id="47ecf-117">**GetCursorCount**</span></span>](itablet-getcursorcount.md)                       | <span data-ttu-id="47ecf-118">Извлекает количество объектов Cursor, связанных с планшетом.</span><span class="sxs-lookup"><span data-stu-id="47ecf-118">Retrieves the number of cursor objects associated with the tablet.</span></span><br/>         |
| [<span data-ttu-id="47ecf-119">**жетдефаултконтекстсеттингс**</span><span class="sxs-lookup"><span data-stu-id="47ecf-119">**GetDefaultContextSettings**</span></span>](itablet-getdefaultcontextsettings.md) | <span data-ttu-id="47ecf-120">Извлекает параметры контекста по умолчанию для планшета.</span><span class="sxs-lookup"><span data-stu-id="47ecf-120">Retrieves the default context settings for the tablet.</span></span><br/>                     |
| [<span data-ttu-id="47ecf-121">**жесардварекапс**</span><span class="sxs-lookup"><span data-stu-id="47ecf-121">**GetHardwareCaps**</span></span>](itablet-gethardwarecaps.md)                     | <span data-ttu-id="47ecf-122">Извлекает значение, представляющее возможности устройства планшета.</span><span class="sxs-lookup"><span data-stu-id="47ecf-122">Retrieves a value that represents the capabilities of the tablet hardware.</span></span><br/> |
| [<span data-ttu-id="47ecf-123">**жетмаксинпутрект**</span><span class="sxs-lookup"><span data-stu-id="47ecf-123">**GetMaxInputRect**</span></span>](itablet-getmaxinputrect.md)                     | <span data-ttu-id="47ecf-124">Извлекает прямоугольник, представляющий максимальную область ввода планшета.</span><span class="sxs-lookup"><span data-stu-id="47ecf-124">Retrieves a rectangle that represents maximum input area of the tablet.</span></span><br/>    |
| [<span data-ttu-id="47ecf-125">**GetName**</span><span class="sxs-lookup"><span data-stu-id="47ecf-125">**GetName**</span></span>](itablet-getname.md)                                     | <span data-ttu-id="47ecf-126">Извлекает строку, содержащую имя устройства планшета.</span><span class="sxs-lookup"><span data-stu-id="47ecf-126">Retrieves a string containing the name of the tablet device.</span></span><br/>               |
| [<span data-ttu-id="47ecf-127">**жетплугандплайид**</span><span class="sxs-lookup"><span data-stu-id="47ecf-127">**GetPlugAndPlayId**</span></span>](itablet-getplugandplayid.md)                   | <span data-ttu-id="47ecf-128">Извлекает строку, содержащую идентификатор самонастраивающийся для устройства планшета.</span><span class="sxs-lookup"><span data-stu-id="47ecf-128">Retrieves a string containing the Plug and Play ID for the tablet device.</span></span><br/>  |
| <span data-ttu-id="47ecf-129">[**жетпропертиметрикс**](/previous-versions/windows/desktop/legacy/aa367722(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="47ecf-129">[**GetPropertyMetrics**](/previous-versions/windows/desktop/legacy/aa367722(v=vs.85))</span></span>               | <span data-ttu-id="47ecf-130">Извлекает данные метрик для указанного свойства.</span><span class="sxs-lookup"><span data-stu-id="47ecf-130">Retrieves the metrics data for a specified property.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="47ecf-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="47ecf-131">Remarks</span></span>

<span data-ttu-id="47ecf-132">Разработчики не должны использовать этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="47ecf-132">Developers should not use this interface.</span></span>

<span data-ttu-id="47ecf-133">В следующем коде показано, как определяется интерфейс **итаблет** .</span><span class="sxs-lookup"><span data-stu-id="47ecf-133">The following code describes how the **ITablet** interface is defined.</span></span>

``` syntax
[
    object,
   uuid(1CB2EFC3-ABC7-4172-8FCB-3BC9CB93E29F),
    pointer_default(unique)
]
interface ITablet : IUnknown
{
    HRESULT GetDefaultContextSettings(
        [out] TABLET_CONTEXT_SETTINGS **ppTCS);

    HRESULT CreateContext(
        [in] HWND hWnd,
        [in, unique] RECT *prcInput,
        [in] DWORD dwOptions,
        [in, unique] TABLET_CONTEXT_SETTINGS *pTCS,
        [in] CONTEXT_ENABLE_TYPE cet,
        [out] ITabletContext **ppCtx,
        [in, out, unique] TABLET_CONTEXT_ID *pTcid,
        [in, out, unique] PACKET_DESCRIPTION **ppPD,
        [in, unique] ITabletEventSink *pSink);

    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetMaxInputRect(
        [out] RECT *prcInput);

    HRESULT GetHardwareCaps(
        [out] DWORD *pdwCaps);

    HRESULT GetPropertyMetrics(
        [in] REFGUID rguid,
        [out] PROPERTY_METRICS *pPM);

    HRESULT GetPlugAndPlayId(
        [out] LPWSTR *ppwszPPId);

    HRESULT GetCursorCount(
        [out] ULONG *pcCurs);

    HRESULT GetCursor(
        [in] ULONG iCur,
        [out] ITabletCursor **ppCur);
};   
```

## <a name="requirements"></a><span data-ttu-id="47ecf-134">Требования</span><span class="sxs-lookup"><span data-stu-id="47ecf-134">Requirements</span></span>



| <span data-ttu-id="47ecf-135">Требование</span><span class="sxs-lookup"><span data-stu-id="47ecf-135">Requirement</span></span> | <span data-ttu-id="47ecf-136">Значение</span><span class="sxs-lookup"><span data-stu-id="47ecf-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47ecf-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="47ecf-137">Minimum supported client</span></span><br/> | <span data-ttu-id="47ecf-138">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="47ecf-138">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="47ecf-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="47ecf-139">Minimum supported server</span></span><br/> | <span data-ttu-id="47ecf-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="47ecf-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="47ecf-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="47ecf-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="47ecf-142"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="47ecf-142"><dt>Wisptis.exe</dt></span></span> </dl> |



 

