---
title: Сообщение TB_CHANGEBITMAP (Коммктрл. h)
description: Изменяет точечный рисунок для кнопки на панели инструментов.
ms.assetid: 112b6f4e-6034-4e13-8b2f-b8411a351fbd
keywords:
- Элементы управления Windows для TB_CHANGEBITMAP сообщений
topic_type:
- apiref
api_name:
- TB_CHANGEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1367a2a1b4e35d6f52bf1e7a0be42f1e75daa7ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892806"
---
# <a name="tb_changebitmap-message"></a><span data-ttu-id="74088-104">\_Сообщение ЧАНЖЕБИТМАП ТБ</span><span class="sxs-lookup"><span data-stu-id="74088-104">TB\_CHANGEBITMAP message</span></span>

<span data-ttu-id="74088-105">Изменяет точечный рисунок для кнопки на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="74088-105">Changes the bitmap for a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="74088-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="74088-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74088-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74088-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74088-108">Идентификатор команды для получения нового точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="74088-108">Command identifier of the button that is to receive a new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="74088-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74088-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74088-110">Отсчитываемый от нуля индекс изображения в списке изображений на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="74088-110">Zero-based index of an image in the toolbar's image list.</span></span> <span data-ttu-id="74088-111">Система отображает указанное изображение в кнопке.</span><span class="sxs-lookup"><span data-stu-id="74088-111">The system displays the specified image in the button.</span></span> <span data-ttu-id="74088-112">Задайте для этого параметра значение I \_ имажекаллбакк, после чего панель инструментов отправит уведомление [**\_ жетдиспинфо ТБН**](tbn-getdispinfo.md) , чтобы получить индекс изображения, когда он понадобится.</span><span class="sxs-lookup"><span data-stu-id="74088-112">Set this parameter to I\_IMAGECALLBACK, and the toolbar will send the [**TBN\_GETDISPINFO**](tbn-getdispinfo.md) notification to retrieve the image index when it is needed.</span></span>

<span data-ttu-id="74088-113">[Версия 5,81](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="74088-113">[Version 5.81](common-control-versions.md).</span></span> <span data-ttu-id="74088-114">Установите этот параметр в значение I \_ имаженоне, чтобы указать, что кнопка не имеет изображения.</span><span class="sxs-lookup"><span data-stu-id="74088-114">Set this parameter to I\_IMAGENONE to indicate that the button does not have an image.</span></span> <span data-ttu-id="74088-115">Макет кнопки не будет содержать пробелы для точечного рисунка, а только для текста.</span><span class="sxs-lookup"><span data-stu-id="74088-115">The button layout will not include any space for a bitmap, only text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74088-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74088-116">Return value</span></span>

<span data-ttu-id="74088-117">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="74088-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="74088-118">Требования</span><span class="sxs-lookup"><span data-stu-id="74088-118">Requirements</span></span>



| <span data-ttu-id="74088-119">Требование</span><span class="sxs-lookup"><span data-stu-id="74088-119">Requirement</span></span> | <span data-ttu-id="74088-120">Значение</span><span class="sxs-lookup"><span data-stu-id="74088-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74088-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74088-121">Minimum supported client</span></span><br/> | <span data-ttu-id="74088-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="74088-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74088-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74088-123">Minimum supported server</span></span><br/> | <span data-ttu-id="74088-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="74088-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74088-125">Header</span><span class="sxs-lookup"><span data-stu-id="74088-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="74088-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="74088-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





