---
title: Сообщение EM_GETIMECOMPMODE (RichEdit. h)
description: Извлекает текущий режим редактора метода ввода (IME) для элемента управления расширенного редактирования.
ms.assetid: dac96833-4c3d-4da7-9ea4-52204434ec10
keywords:
- Элементы управления Windows для EM_GETIMECOMPMODE сообщений
topic_type:
- apiref
api_name:
- EM_GETIMECOMPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feb2f5f31831e0e292bf002f24ca4978f25753a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491805"
---
# <a name="em_getimecompmode-message"></a><span data-ttu-id="8daba-104">\_Сообщение ЖЕТИМЕКОМПМОДЕ EM</span><span class="sxs-lookup"><span data-stu-id="8daba-104">EM\_GETIMECOMPMODE message</span></span>

<span data-ttu-id="8daba-105">Извлекает текущий режим редактора метода ввода (IME) для элемента управления расширенного редактирования.</span><span class="sxs-lookup"><span data-stu-id="8daba-105">Retrieves the current Input Method Editor (IME) mode for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8daba-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8daba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8daba-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8daba-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8daba-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="8daba-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8daba-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8daba-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8daba-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="8daba-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8daba-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8daba-111">Return value</span></span>

<span data-ttu-id="8daba-112">Возвращаемое значение является одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="8daba-112">The return value is one of the following values.</span></span>



| <span data-ttu-id="8daba-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8daba-113">Return code</span></span>                                                                                     | <span data-ttu-id="8daba-114">Описание</span><span class="sxs-lookup"><span data-stu-id="8daba-114">Description</span></span>                  |
|-------------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="8daba-115"><dt>**ICM \_ нотопен**</dt></span><span class="sxs-lookup"><span data-stu-id="8daba-115"><dt>**ICM\_NOTOPEN**</dt></span></span> </dl>     | <span data-ttu-id="8daba-116">Редактор IME не открыт.</span><span class="sxs-lookup"><span data-stu-id="8daba-116">IME is not open.</span></span><br/>  |
| <dl> <span data-ttu-id="8daba-117"><dt>**ICM \_ LEVEL3**</dt></span><span class="sxs-lookup"><span data-stu-id="8daba-117"><dt>**ICM\_LEVEL3**</dt></span></span> </dl>      | <span data-ttu-id="8daba-118">Истинный встроенный режим.</span><span class="sxs-lookup"><span data-stu-id="8daba-118">True inline mode.</span></span><br/> |
| <dl> <span data-ttu-id="8daba-119"><dt>**ICM \_ level2**</dt></span><span class="sxs-lookup"><span data-stu-id="8daba-119"><dt>**ICM\_LEVEL2**</dt></span></span> </dl>      | <span data-ttu-id="8daba-120">Уровень 2.</span><span class="sxs-lookup"><span data-stu-id="8daba-120">Level 2.</span></span><br/>          |
| <dl> <span data-ttu-id="8daba-121"><dt>**ICM \_ level2 \_ 5**</dt></span><span class="sxs-lookup"><span data-stu-id="8daba-121"><dt>**ICM\_LEVEL2\_5**</dt></span></span> </dl>   | <span data-ttu-id="8daba-122">Уровень 2,5</span><span class="sxs-lookup"><span data-stu-id="8daba-122">Level 2.5</span></span><br/>         |
| <dl> <span data-ttu-id="8daba-123"><dt>**ICM \_ level2 \_ СУИ**</dt></span><span class="sxs-lookup"><span data-stu-id="8daba-123"><dt>**ICM\_LEVEL2\_SUI**</dt></span></span> </dl> | <span data-ttu-id="8daba-124">Специальный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="8daba-124">Special UI.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="8daba-125">Требования</span><span class="sxs-lookup"><span data-stu-id="8daba-125">Requirements</span></span>



| <span data-ttu-id="8daba-126">Требование</span><span class="sxs-lookup"><span data-stu-id="8daba-126">Requirement</span></span> | <span data-ttu-id="8daba-127">Значение</span><span class="sxs-lookup"><span data-stu-id="8daba-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8daba-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8daba-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8daba-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8daba-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8daba-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8daba-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8daba-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8daba-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8daba-132">Header</span><span class="sxs-lookup"><span data-stu-id="8daba-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8daba-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8daba-133"><dt>Richedit.h</dt></span></span> </dl> |



 

 





