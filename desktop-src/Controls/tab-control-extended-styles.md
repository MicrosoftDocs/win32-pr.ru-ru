---
title: Расширенные стили элемента управления Tab (Коммктрл. h)
description: Теперь элемент управления "Вкладка" поддерживает расширенные стили. Эти стили управляются с помощью сообщений TCM \_ жетекстендедстиле и TCM \_ сетекстендедстиле, и их не следует путать с расширенными стилями окон, передаваемыми в CreateWindowEx.
ms.assetid: 24294037-598c-4fcd-8a7c-8647ccfb1d81
topic_type:
- apiref
api_name:
- TCS_EX_FLATSEPARATORS
- TCS_EX_REGISTERDROP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c4e16b40a394bc9b808386d3cbdc3abf9b3d928
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648685"
---
# <a name="tab-control-extended-styles"></a><span data-ttu-id="5df25-104">Расширенные стили элемента управления Tab</span><span class="sxs-lookup"><span data-stu-id="5df25-104">Tab Control Extended Styles</span></span>

<span data-ttu-id="5df25-105">Теперь элемент управления "Вкладка" поддерживает расширенные стили.</span><span class="sxs-lookup"><span data-stu-id="5df25-105">The tab control now supports extended styles.</span></span> <span data-ttu-id="5df25-106">Эти стили управляются с помощью сообщений [**TCM \_ Жетекстендедстиле**](tcm-getextendedstyle.md) и [**TCM \_ сетекстендедстиле**](tcm-setextendedstyle.md) , и их не следует путать с расширенными стилями окон, передаваемыми в [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span><span class="sxs-lookup"><span data-stu-id="5df25-106">These styles are manipulated using the [**TCM\_GETEXTENDEDSTYLE**](tcm-getextendedstyle.md) and [**TCM\_SETEXTENDEDSTYLE**](tcm-setextendedstyle.md) messages and should not be confused with extended window styles that are passed to [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span>



| <span data-ttu-id="5df25-107">Константа</span><span class="sxs-lookup"><span data-stu-id="5df25-107">Constant</span></span>                                                                                                                                                                               | <span data-ttu-id="5df25-108">Описание</span><span class="sxs-lookup"><span data-stu-id="5df25-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_EX_FLATSEPARATORS"></span><span id="tcs_ex_flatseparators"></span><dl> <span data-ttu-id="5df25-109"><dt>**TCS \_ ex \_ флатсепараторс**</dt></span><span class="sxs-lookup"><span data-stu-id="5df25-109"><dt>**TCS\_EX\_FLATSEPARATORS**</dt></span></span> </dl> | <span data-ttu-id="5df25-110">[Версия 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="5df25-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="5df25-111">Элемент управления "Вкладка" будет рисовать разделители между элементами вкладки.</span><span class="sxs-lookup"><span data-stu-id="5df25-111">The tab control will draw separators between the tab items.</span></span> <span data-ttu-id="5df25-112">Этот расширенный стиль влияет только на элементы управления "Вкладка", у которых есть [**\_ кнопки TCS**](tab-control-styles.md) и [**TCS \_ флатбуттонс**](tab-control-styles.md) Styles.</span><span class="sxs-lookup"><span data-stu-id="5df25-112">This extended style only affects tab controls that have the [**TCS\_BUTTONS**](tab-control-styles.md) and [**TCS\_FLATBUTTONS**](tab-control-styles.md) styles.</span></span> <span data-ttu-id="5df25-113">По умолчанию создание элемента управления "Вкладка" с помощью стиля **TCS \_ флатбуттонс** задает этот расширенный стиль.</span><span class="sxs-lookup"><span data-stu-id="5df25-113">By default, creating the tab control with the **TCS\_FLATBUTTONS** style sets this extended style.</span></span> <span data-ttu-id="5df25-114">Если разделители не требуются, этот расширенный стиль следует удалить после создания элемента управления.</span><span class="sxs-lookup"><span data-stu-id="5df25-114">If you do not require separators, you should remove this extended style after creating the control.</span></span><br/> |
| <span id="TCS_EX_REGISTERDROP"></span><span id="tcs_ex_registerdrop"></span><dl> <span data-ttu-id="5df25-115"><dt>**TCS \_ ex \_ регистердроп**</dt></span><span class="sxs-lookup"><span data-stu-id="5df25-115"><dt>**TCS\_EX\_REGISTERDROP**</dt></span></span> </dl>       | <span data-ttu-id="5df25-116">[Версия 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="5df25-116">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="5df25-117">Элемент управления "Вкладка" создает коды уведомлений [ТКН \_ GetObject](tcn-getobject.md) для запроса целевого объекта перетаскивания при перетаскивании объекта на элементы вкладки в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="5df25-117">The tab control generates [TCN\_GETOBJECT](tcn-getobject.md) notification codes to request a drop target object when an object is dragged over the tab items in the control.</span></span> <span data-ttu-id="5df25-118">Перед установкой этого стиля приложение должно вызвать [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) или [**олеинитиализе**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) .</span><span class="sxs-lookup"><span data-stu-id="5df25-118">The application must call [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) before setting this style.</span></span> <br/>                                                                                                                                               |



## <a name="requirements"></a><span data-ttu-id="5df25-119">Требования</span><span class="sxs-lookup"><span data-stu-id="5df25-119">Requirements</span></span>



| <span data-ttu-id="5df25-120">Требование</span><span class="sxs-lookup"><span data-stu-id="5df25-120">Requirement</span></span> | <span data-ttu-id="5df25-121">Значение</span><span class="sxs-lookup"><span data-stu-id="5df25-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5df25-122">Header</span><span class="sxs-lookup"><span data-stu-id="5df25-122">Header</span></span><br/> | <dl> <span data-ttu-id="5df25-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="5df25-123"><dt>CommCtrl.h</dt></span></span> </dl> |



 

