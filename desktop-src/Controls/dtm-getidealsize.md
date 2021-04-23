---
title: Сообщение DTM_GETIDEALSIZE (Коммктрл. h)
description: Возвращает размер, необходимый для вывода элемента управления без усечения. Отправляйте это сообщение явным образом или с помощью \_ макроса DateTime жетидеалсизе.
ms.assetid: 15ec26a1-645b-4a96-af66-1031e1a46c6c
keywords:
- Элементы управления Windows для DTM_GETIDEALSIZE сообщений
topic_type:
- apiref
api_name:
- DTM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a979883f431fea4627f52fe19c3716341e3f2328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262187"
---
# <a name="dtm_getidealsize-message"></a><span data-ttu-id="318b6-105">\_Сообщение DTM жетидеалсизе</span><span class="sxs-lookup"><span data-stu-id="318b6-105">DTM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="318b6-106">Возвращает размер, необходимый для вывода элемента управления без усечения.</span><span class="sxs-lookup"><span data-stu-id="318b6-106">Gets the size needed to display the control without clipping.</span></span> <span data-ttu-id="318b6-107">Отправляйте это сообщение явным образом или с помощью макроса [**DateTime \_ жетидеалсизе**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) .</span><span class="sxs-lookup"><span data-stu-id="318b6-107">Send this message explicitly or by using the [**DateTime\_GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="318b6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="318b6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="318b6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="318b6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="318b6-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="318b6-110">Not used.</span></span> <span data-ttu-id="318b6-111">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="318b6-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="318b6-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="318b6-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="318b6-113">Указатель на структуру [**размера**](/previous-versions//dd145106(v=vs.85)) для получения идеального размера.</span><span class="sxs-lookup"><span data-stu-id="318b6-113">A pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure to receive the ideal size.</span></span> <span data-ttu-id="318b6-114">Вызывающее приложение отвечает за выделение этой структуры.</span><span class="sxs-lookup"><span data-stu-id="318b6-114">The calling application is responsible for allocating this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="318b6-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="318b6-115">Return value</span></span>

<span data-ttu-id="318b6-116">Возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="318b6-116">Returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="318b6-117">Требования</span><span class="sxs-lookup"><span data-stu-id="318b6-117">Requirements</span></span>



| <span data-ttu-id="318b6-118">Требование</span><span class="sxs-lookup"><span data-stu-id="318b6-118">Requirement</span></span> | <span data-ttu-id="318b6-119">Значение</span><span class="sxs-lookup"><span data-stu-id="318b6-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="318b6-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="318b6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="318b6-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="318b6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="318b6-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="318b6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="318b6-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="318b6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="318b6-124">Header</span><span class="sxs-lookup"><span data-stu-id="318b6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="318b6-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="318b6-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

