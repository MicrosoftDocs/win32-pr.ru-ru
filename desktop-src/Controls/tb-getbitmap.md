---
title: Сообщение TB_GETBITMAP (Коммктрл. h)
description: Извлекает индекс растрового изображения, связанного с кнопкой на панели инструментов.
ms.assetid: 64878cca-7d71-48ad-b2ed-d2bdc3067592
keywords:
- Элементы управления Windows для TB_GETBITMAP сообщений
topic_type:
- apiref
api_name:
- TB_GETBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771073b67b1421a5d9bda9d162bc234400c85885
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989437"
---
# <a name="tb_getbitmap-message"></a><span data-ttu-id="6ac34-104">(ТБ) \_ сообщение с изображением</span><span class="sxs-lookup"><span data-stu-id="6ac34-104">TB\_GETBITMAP message</span></span>

<span data-ttu-id="6ac34-105">Извлекает индекс растрового изображения, связанного с кнопкой на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="6ac34-105">Retrieves the index of the bitmap associated with a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="6ac34-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ac34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ac34-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6ac34-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ac34-108">Идентификатор команды для кнопки, индекс которой необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="6ac34-108">Command identifier of the button whose bitmap index is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="6ac34-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ac34-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6ac34-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="6ac34-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ac34-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ac34-111">Return value</span></span>

<span data-ttu-id="6ac34-112">Возвращает индекс битовой карты в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6ac34-112">Returns the index of the bitmap if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ac34-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6ac34-113">Requirements</span></span>



| <span data-ttu-id="6ac34-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6ac34-114">Requirement</span></span> | <span data-ttu-id="6ac34-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6ac34-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ac34-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ac34-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6ac34-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6ac34-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6ac34-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ac34-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6ac34-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6ac34-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6ac34-120">Header</span><span class="sxs-lookup"><span data-stu-id="6ac34-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ac34-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ac34-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





