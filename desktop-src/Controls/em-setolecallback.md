---
title: Сообщение EM_SETOLECALLBACK (RichEdit. h)
description: Предоставляет форматируемый элемент управления "поле ввода", объект Иричедитолекаллбакк, используемый элементом управления для получения связанных с OLE ресурсов и информации от клиента.
ms.assetid: bd1f8048-214c-4ac6-b826-bedabb1aaee5
keywords:
- Элементы управления Windows для EM_SETOLECALLBACK сообщений
topic_type:
- apiref
api_name:
- EM_SETOLECALLBACK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfc54db112bba42fc3d51b2e328fc7641990c7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988824"
---
# <a name="em_setolecallback-message"></a><span data-ttu-id="9a891-104">\_Сообщение СЕТОЛЕКАЛЛБАКК EM</span><span class="sxs-lookup"><span data-stu-id="9a891-104">EM\_SETOLECALLBACK message</span></span>

<span data-ttu-id="9a891-105">Предоставляет форматируемый элемент управления "поле ввода", объект [**иричедитолекаллбакк**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) , используемый элементом управления для получения связанных с OLE ресурсов и информации от клиента.</span><span class="sxs-lookup"><span data-stu-id="9a891-105">Gives a rich edit control an [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) object that the control uses to get OLE-related resources and information from the client.</span></span>

## <a name="parameters"></a><span data-ttu-id="9a891-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a891-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a891-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9a891-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a891-108">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="9a891-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9a891-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a891-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a891-110">Указатель на объект [**иричедитолекаллбакк**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) .</span><span class="sxs-lookup"><span data-stu-id="9a891-110">Pointer to an [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) object.</span></span> <span data-ttu-id="9a891-111">Перед возвратом элемент управления вызывает метод [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) для объекта.</span><span class="sxs-lookup"><span data-stu-id="9a891-111">The control calls the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) method for the object before returning.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a891-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a891-112">Return value</span></span>

<span data-ttu-id="9a891-113">Если операция завершилась удачно, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="9a891-113">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="9a891-114">Если операция завершается ошибкой, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="9a891-114">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a891-115">Требования</span><span class="sxs-lookup"><span data-stu-id="9a891-115">Requirements</span></span>



| <span data-ttu-id="9a891-116">Требование</span><span class="sxs-lookup"><span data-stu-id="9a891-116">Requirement</span></span> | <span data-ttu-id="9a891-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9a891-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a891-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9a891-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9a891-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9a891-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9a891-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9a891-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9a891-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9a891-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9a891-122">Header</span><span class="sxs-lookup"><span data-stu-id="9a891-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a891-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a891-123"><dt>Richedit.h</dt></span></span> </dl> |



 

