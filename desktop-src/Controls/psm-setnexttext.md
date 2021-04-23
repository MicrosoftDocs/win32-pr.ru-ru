---
title: Сообщение PSM_SETNEXTTEXT (Пршт. h)
description: Задает текст кнопки "Далее" в мастере. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит сетнексттекст.
ms.assetid: 4608425e-1724-4d0b-b0f6-9fec147a85f6
keywords:
- Элементы управления Windows для PSM_SETNEXTTEXT сообщений
topic_type:
- apiref
api_name:
- PSM_SETNEXTTEXT
- PSM_SETNEXTTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d781a8d76fca5c1e74bcda452b6ab7e03a32aacc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801222"
---
# <a name="psm_setnexttext-message"></a><span data-ttu-id="4759a-105">\_Сообщение ПСМ сетнексттекст</span><span class="sxs-lookup"><span data-stu-id="4759a-105">PSM\_SETNEXTTEXT message</span></span>

<span data-ttu-id="4759a-106">Задает текст кнопки " **Далее** " в мастере.</span><span class="sxs-lookup"><span data-stu-id="4759a-106">Sets the text of the **Next** button in a wizard.</span></span> <span data-ttu-id="4759a-107">Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ сетнексттекст**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) .</span><span class="sxs-lookup"><span data-stu-id="4759a-107">You can send this message explicitly or by using the [**PropSheet\_SetNextText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4759a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4759a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4759a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4759a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4759a-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="4759a-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4759a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4759a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4759a-112">Указатель на буфер, содержащий текст.</span><span class="sxs-lookup"><span data-stu-id="4759a-112">Pointer to a buffer that contains the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4759a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4759a-113">Return value</span></span>

<span data-ttu-id="4759a-114">Нет осмысленных возвращаемых значений.</span><span class="sxs-lookup"><span data-stu-id="4759a-114">No meaningful return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4759a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4759a-115">Requirements</span></span>



| <span data-ttu-id="4759a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4759a-116">Requirement</span></span> | <span data-ttu-id="4759a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4759a-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4759a-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4759a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4759a-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4759a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4759a-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4759a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4759a-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4759a-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4759a-122">Header</span><span class="sxs-lookup"><span data-stu-id="4759a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4759a-123"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="4759a-123"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="4759a-124">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="4759a-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4759a-125">**ПСМ \_ СЕТНЕКСТТЕКСТВ** (Юникод)</span><span class="sxs-lookup"><span data-stu-id="4759a-125">**PSM\_SETNEXTTEXTW** (Unicode)</span></span><br/>                                         |



 

 





