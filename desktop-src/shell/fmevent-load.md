---
description: Отправляется в библиотеку DLL расширения, когда диспетчер файлов загружает библиотеку DLL.
ms.assetid: 9d673ab8-c468-4b46-b96e-1adfaa9f85fb
title: Сообщение FMEVENT_LOAD (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: de7a950e3f17c9b2cee2b66a047d289ca29b6b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985513"
---
# <a name="fmevent_load-message"></a><span data-ttu-id="79530-103">\_Сообщение о загрузке фмевент</span><span class="sxs-lookup"><span data-stu-id="79530-103">FMEVENT\_LOAD message</span></span>

<span data-ttu-id="79530-104">Отправляется в библиотеку DLL расширения, когда диспетчер файлов загружает библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="79530-104">Sent to an extension DLL when File Manager is loading the DLL.</span></span>

## <a name="parameters"></a><span data-ttu-id="79530-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="79530-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79530-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="79530-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79530-107">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="79530-107">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="79530-108">*лпфмслд*</span><span class="sxs-lookup"><span data-stu-id="79530-108">*lpfmsld*</span></span> 
</dt> <dd>

<span data-ttu-id="79530-109">Адрес структуры [**\_ загрузки FMS**](fms-load.md) , указывающей разностное значение пункта меню.</span><span class="sxs-lookup"><span data-stu-id="79530-109">The address of an [**FMS\_LOAD**](fms-load.md) structure that specifies the menu item delta value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79530-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79530-110">Return value</span></span>

<span data-ttu-id="79530-111">Библиотека DLL расширения должна возвращать **значение true** , чтобы продолжить загрузку библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="79530-111">An extension DLL must return **TRUE** to continue loading the DLL.</span></span> <span data-ttu-id="79530-112">Если библиотека DLL возвращает **значение false**, диспетчер файлов вызывает функцию [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) и завершает все взаимодействие с библиотекой DLL расширения.</span><span class="sxs-lookup"><span data-stu-id="79530-112">If the DLL returns **FALSE**, File Manager calls the [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) function and ends any communication with the extension DLL.</span></span>

## <a name="remarks"></a><span data-ttu-id="79530-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="79530-113">Remarks</span></span>

<span data-ttu-id="79530-114">Приложение должно заполнить элементы **двсизе**, **сзменунаме** и **HMENU** в структуре [**\_ загрузки FMS**](fms-load.md) .</span><span class="sxs-lookup"><span data-stu-id="79530-114">An application should fill the **dwSize**, **szMenuName**, and **hMenu** members in the [**FMS\_LOAD**](fms-load.md) structure.</span></span> <span data-ttu-id="79530-115">Он также должен сохранить значение элемента **вменуделта** и использовать его для обнаружения пунктов меню при изменении меню.</span><span class="sxs-lookup"><span data-stu-id="79530-115">It should also save the value of the **wMenuDelta** member and use it to identify menu items when modifying the menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="79530-116">Требования</span><span class="sxs-lookup"><span data-stu-id="79530-116">Requirements</span></span>



| <span data-ttu-id="79530-117">Требование</span><span class="sxs-lookup"><span data-stu-id="79530-117">Requirement</span></span> | <span data-ttu-id="79530-118">Значение</span><span class="sxs-lookup"><span data-stu-id="79530-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="79530-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79530-119">Minimum supported client</span></span><br/> | <span data-ttu-id="79530-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="79530-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="79530-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79530-121">Minimum supported server</span></span><br/> | <span data-ttu-id="79530-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="79530-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="79530-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="79530-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="79530-124"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="79530-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79530-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79530-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79530-126">**фмекстенсионпрок**</span><span class="sxs-lookup"><span data-stu-id="79530-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 
