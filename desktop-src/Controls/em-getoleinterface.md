---
title: Сообщение EM_GETOLEINTERFACE (RichEdit. h)
description: Извлекает объект Иричедитоле, который клиент может использовать для доступа к функциональным возможностям модели COM в элементе управления "поле ввода".
ms.assetid: fa462c7b-29b9-4694-b7ad-6068c69ffb76
keywords:
- Элементы управления Windows для EM_GETOLEINTERFACE сообщений
topic_type:
- apiref
api_name:
- EM_GETOLEINTERFACE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d7557d40c6dcec38ce629d949a8db9915714821
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136658"
---
# <a name="em_getoleinterface-message"></a><span data-ttu-id="024e2-104">\_Сообщение ЖЕТОЛЕИНТЕРФАЦЕ EM</span><span class="sxs-lookup"><span data-stu-id="024e2-104">EM\_GETOLEINTERFACE message</span></span>

<span data-ttu-id="024e2-105">Извлекает объект [**иричедитоле**](/windows/desktop/api/Richole/nn-richole-iricheditole) , который клиент может использовать для доступа к функциональным ВОЗМОЖНОСТЯМ модели COM в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="024e2-105">Retrieves an [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) object that a client can use to access a rich edit control's Component Object Model (COM) functionality.</span></span>

## <a name="parameters"></a><span data-ttu-id="024e2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="024e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="024e2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="024e2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="024e2-108">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="024e2-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="024e2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="024e2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="024e2-110">Указатель на указатель, который получает объект [**иричедитоле**](/windows/desktop/api/Richole/nn-richole-iricheditole) .</span><span class="sxs-lookup"><span data-stu-id="024e2-110">Pointer to a pointer that receives the [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) object.</span></span> <span data-ttu-id="024e2-111">Перед возвратом элемент управления вызывает метод [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) для объекта, поэтому вызывающее приложение должно вызвать метод [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) , когда он завершит работу с объектом.</span><span class="sxs-lookup"><span data-stu-id="024e2-111">The control calls the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) method for the object before returning, so the calling application must call the [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) method when it is done with the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="024e2-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="024e2-112">Return value</span></span>

<span data-ttu-id="024e2-113">Если операция завершилась удачно, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="024e2-113">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="024e2-114">Если операция завершается ошибкой, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="024e2-114">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="024e2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="024e2-115">Requirements</span></span>



| <span data-ttu-id="024e2-116">Требование</span><span class="sxs-lookup"><span data-stu-id="024e2-116">Requirement</span></span> | <span data-ttu-id="024e2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="024e2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="024e2-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="024e2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="024e2-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="024e2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="024e2-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="024e2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="024e2-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="024e2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="024e2-122">Header</span><span class="sxs-lookup"><span data-stu-id="024e2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="024e2-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="024e2-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="024e2-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="024e2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="024e2-125">**иричедитоле**</span><span class="sxs-lookup"><span data-stu-id="024e2-125">**IRichEditOle**</span></span>](/windows/desktop/api/Richole/nn-richole-iricheditole)
</dt> </dl>

 

