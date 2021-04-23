---
title: External. Довнлоадманажер
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается. Свойство Довнлоадманажер извлекает объект Довнлоадманажер.
ms.assetid: 9fec7175-611e-4e7e-8978-132e6f86329a
keywords:
- Внешний Довнлоадманажер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- External.DownloadManager
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55e6371f5c8d1e5dfcb17762340a82e8d921c17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695098"
---
# <a name="externaldownloadmanager"></a><span data-ttu-id="abe12-106">External. Довнлоадманажер</span><span class="sxs-lookup"><span data-stu-id="abe12-106">External.DownloadManager</span></span>

> [!Note]  
> <span data-ttu-id="abe12-107">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="abe12-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="abe12-108">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="abe12-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="abe12-109">Свойство **довнлоадманажер** извлекает объект **довнлоадманажер** .</span><span class="sxs-lookup"><span data-stu-id="abe12-109">The **DownloadManager** property retrieves the **DownloadManager** object.</span></span>

``` syntax
window.external.DownloadManager
      
```

## <a name="possible-values"></a><span data-ttu-id="abe12-110">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="abe12-110">Possible Values</span></span>

<span data-ttu-id="abe12-111">Это свойство является объектом **довнлоадманажер** , предназначенным только для чтения.</span><span class="sxs-lookup"><span data-stu-id="abe12-111">This property is a read-only **DownloadManager** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="abe12-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="abe12-112">Remarks</span></span>

<span data-ttu-id="abe12-113">В проигрывателе Windows Media 10 или более поздней версии свойство **довнлоадманажер** и объект доступны только из областей задач службы "Интернет-магазин".</span><span class="sxs-lookup"><span data-stu-id="abe12-113">In Windows Media Player 10 or later, the **DownloadManager** property and object are accessible only from online store service task panes.</span></span> <span data-ttu-id="abe12-114">Нельзя использовать **довнлоадманажер** из других функций, где доступен **внешний** объект, например Хтмлвиев, представление информационной центра и сведения о диске.</span><span class="sxs-lookup"><span data-stu-id="abe12-114">You cannot use the **DownloadManager** from other features where the **External** object is available, such as HTMLView, Info Center View, and album information.</span></span>

## <a name="requirements"></a><span data-ttu-id="abe12-115">Требования</span><span class="sxs-lookup"><span data-stu-id="abe12-115">Requirements</span></span>



| <span data-ttu-id="abe12-116">Требование</span><span class="sxs-lookup"><span data-stu-id="abe12-116">Requirement</span></span> | <span data-ttu-id="abe12-117">Значение</span><span class="sxs-lookup"><span data-stu-id="abe12-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="abe12-118">Версия</span><span class="sxs-lookup"><span data-stu-id="abe12-118">Version</span></span><br/> | <span data-ttu-id="abe12-119">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="abe12-119">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="abe12-120">DLL</span><span class="sxs-lookup"><span data-stu-id="abe12-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="abe12-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abe12-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abe12-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abe12-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abe12-123">**Внешний объект для Интернет-магазинов типа 2**</span><span class="sxs-lookup"><span data-stu-id="abe12-123">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





