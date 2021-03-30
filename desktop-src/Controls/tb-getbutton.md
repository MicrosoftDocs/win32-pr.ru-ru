---
title: Сообщение TB_GETBUTTON (Коммктрл. h)
description: Извлекает сведения об указанной кнопке на панели инструментов.
ms.assetid: d90d053c-0daf-4a5a-b7ca-b9b4472c65a3
keywords:
- Элементы управления Windows для TB_GETBUTTON сообщений
topic_type:
- apiref
api_name:
- TB_GETBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2080a6c984bb2384f68a1388bd46fe598f5087
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804121"
---
# <a name="tb_getbutton-message"></a><span data-ttu-id="4b0ef-104">\_Сообщение о кнопке ТБ</span><span class="sxs-lookup"><span data-stu-id="4b0ef-104">TB\_GETBUTTON message</span></span>

<span data-ttu-id="4b0ef-105">Извлекает сведения об указанной кнопке на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="4b0ef-105">Retrieves information about the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="4b0ef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b0ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b0ef-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4b0ef-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b0ef-108">Отсчитываемый от нуля индекс кнопки, для которой требуется получить сведения.</span><span class="sxs-lookup"><span data-stu-id="4b0ef-108">Zero-based index of the button for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="4b0ef-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4b0ef-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b0ef-110">Указатель на структуру [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) , которая получает сведения о кнопке.</span><span class="sxs-lookup"><span data-stu-id="4b0ef-110">Pointer to the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure that receives the button information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b0ef-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b0ef-111">Return value</span></span>

<span data-ttu-id="4b0ef-112">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4b0ef-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b0ef-113">Требования</span><span class="sxs-lookup"><span data-stu-id="4b0ef-113">Requirements</span></span>



| <span data-ttu-id="4b0ef-114">Требование</span><span class="sxs-lookup"><span data-stu-id="4b0ef-114">Requirement</span></span> | <span data-ttu-id="4b0ef-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4b0ef-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b0ef-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b0ef-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4b0ef-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4b0ef-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4b0ef-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b0ef-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4b0ef-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4b0ef-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4b0ef-120">Header</span><span class="sxs-lookup"><span data-stu-id="4b0ef-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b0ef-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b0ef-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





