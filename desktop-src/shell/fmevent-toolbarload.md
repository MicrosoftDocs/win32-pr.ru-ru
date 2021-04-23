---
description: Отправляется в библиотеку DLL расширения, когда диспетчер файлов загружает панель инструментов. Это сообщение позволяет библиотеке DLL расширения добавить кнопку на панель инструментов диспетчера файлов.
title: Сообщение FMEVENT_TOOLBARLOAD (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c5daab49-4ed5-439b-b1b7-a87f70c379f0
ms.openlocfilehash: 5f04b524c8d44d987513b6605f9f827336078d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264433"
---
# <a name="fmevent_toolbarload-message"></a><span data-ttu-id="f8497-104">\_Сообщение фмевент тулбарлоад</span><span class="sxs-lookup"><span data-stu-id="f8497-104">FMEVENT\_TOOLBARLOAD message</span></span>

<span data-ttu-id="f8497-105">Отправляется в библиотеку DLL расширения, когда диспетчер файлов загружает панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="f8497-105">Sent to an extension DLL when File Manager is loading its toolbar.</span></span> <span data-ttu-id="f8497-106">Это сообщение позволяет библиотеке DLL расширения добавить кнопку на панель инструментов диспетчера файлов.</span><span class="sxs-lookup"><span data-stu-id="f8497-106">This message allows an extension DLL to add a button to the File Manager toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f8497-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8497-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8497-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8497-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f8497-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="f8497-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f8497-110">*лпфмстбл*</span><span class="sxs-lookup"><span data-stu-id="f8497-110">*lpfmstbl*</span></span> 
</dt> <dd>

<span data-ttu-id="f8497-111">Адрес структуры [**FMS \_ тулбарлоад**](fms-toolbarload.md) .</span><span class="sxs-lookup"><span data-stu-id="f8497-111">The address of an [**FMS\_TOOLBARLOAD**](fms-toolbarload.md) structure.</span></span> <span data-ttu-id="f8497-112">Если библиотека DLL расширения добавляет кнопку на панель инструментов в диспетчере файлов, Библиотека DLL должна заполнить структуру сведениями о кнопке.</span><span class="sxs-lookup"><span data-stu-id="f8497-112">If the extension DLL adds a button to the toolbar in File Manager, the DLL should fill the structure with information about the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8497-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8497-113">Return value</span></span>

<span data-ttu-id="f8497-114">Библиотека DLL расширения должна возвращать **значение true** , чтобы добавить кнопку на панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="f8497-114">An extension DLL must return **TRUE** to add the button to the toolbar.</span></span> <span data-ttu-id="f8497-115">Если библиотека DLL возвращает **значение false**, то диспетчер файлов не добавляет кнопку.</span><span class="sxs-lookup"><span data-stu-id="f8497-115">If the DLL returns **FALSE**, File Manager does not add the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8497-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f8497-116">Requirements</span></span>



| <span data-ttu-id="f8497-117">Требование</span><span class="sxs-lookup"><span data-stu-id="f8497-117">Requirement</span></span> | <span data-ttu-id="f8497-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f8497-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f8497-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8497-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f8497-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f8497-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="f8497-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8497-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f8497-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f8497-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f8497-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f8497-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8497-124"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8497-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8497-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8497-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8497-126">**фмекстенсионпрок**</span><span class="sxs-lookup"><span data-stu-id="f8497-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




