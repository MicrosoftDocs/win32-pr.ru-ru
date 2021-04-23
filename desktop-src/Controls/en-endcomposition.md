---
title: Код уведомления EN_ENDCOMPOSITION (RichEdit. h)
description: Сообщает родительскому окну форматированного элемента управления, что пользователь вводит новые данные, или завершил ввод данных при использовании IME или платформы текстовых служб.
ms.assetid: 3956313F-F82F-41A2-AEDA-52E63218977C
keywords:
- EN_ENDCOMPOSITION кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_ENDCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df1c2b5d08b2da73c67edeb6fe7ca4ac639000c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489282"
---
# <a name="en_endcomposition-notification-code"></a><span data-ttu-id="4ef90-104">\_Код уведомления EN ендкомпоситион</span><span class="sxs-lookup"><span data-stu-id="4ef90-104">EN\_ENDCOMPOSITION notification code</span></span>

<span data-ttu-id="4ef90-105">Сообщает родительскому окну форматированного элемента управления, что пользователь вводит новые данные, или завершил ввод данных при использовании IME или [платформы текстовых служб](/windows/desktop/TSF/text-services-framework).</span><span class="sxs-lookup"><span data-stu-id="4ef90-105">Notifies a rich edit control parent window that the user has entered new data or has finished entering data while using IME or [Text Services Framework](/windows/desktop/TSF/text-services-framework).</span></span>


```C++
EN_ENDCOMPOSITION

     pEndComp = (ENDCOMPOSITIONNOTIFY *)lParam;
```



## <a name="parameters"></a><span data-ttu-id="4ef90-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ef90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ef90-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4ef90-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ef90-108">Структура [**ендкомпоситионнотифи**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify) , которая получает сведения о условии End композиция.</span><span class="sxs-lookup"><span data-stu-id="4ef90-108">A [**ENDCOMPOSITIONNOTIFY**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify) structure that receives information about the end composition condition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ef90-109">Требования</span><span class="sxs-lookup"><span data-stu-id="4ef90-109">Requirements</span></span>



| <span data-ttu-id="4ef90-110">Требование</span><span class="sxs-lookup"><span data-stu-id="4ef90-110">Requirement</span></span> | <span data-ttu-id="4ef90-111">Значение</span><span class="sxs-lookup"><span data-stu-id="4ef90-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4ef90-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4ef90-112">Minimum supported client</span></span><br/> | <span data-ttu-id="4ef90-113">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4ef90-113">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4ef90-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4ef90-114">Minimum supported server</span></span><br/> | <span data-ttu-id="4ef90-115">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4ef90-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4ef90-116">Header</span><span class="sxs-lookup"><span data-stu-id="4ef90-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ef90-117"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ef90-117"><dt>Richedit.h</dt></span></span> </dl> |



 

