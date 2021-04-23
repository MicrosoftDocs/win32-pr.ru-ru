---
description: Включает или отключает режим предварительного просмотра, который позволяет приложению перезаписать начальную логику буферизации.
ms.assetid: 8aa8c6ac-8746-4bf6-9f57-b1426495a275
title: Свойство MFNETSOURCE_PREVIEWMODEENABLED (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1170135b0feb90a79bf5e26d36a02e262fdc1977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650988"
---
# <a name="mfnetsource_previewmodeenabled-property"></a><span data-ttu-id="04a72-103">МФНЕТСАУРЦЕ \_ превиевмодинаблед, свойство</span><span class="sxs-lookup"><span data-stu-id="04a72-103">MFNETSOURCE\_PREVIEWMODEENABLED property</span></span>

<span data-ttu-id="04a72-104">Включает или отключает режим предварительного просмотра, который позволяет приложению перезаписать начальную логику буферизации.</span><span class="sxs-lookup"><span data-stu-id="04a72-104">Enables or disables preview mode, which enables the application to overwrite the initial buffering logic.</span></span>



<span data-ttu-id="04a72-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="04a72-105">Data type</span></span>

<span data-ttu-id="04a72-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="04a72-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="04a72-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="04a72-107">PROPVARIANT member</span></span>

<span data-ttu-id="04a72-108">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="04a72-108">**BOOL**</span></span>

<span data-ttu-id="04a72-109">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="04a72-109">VT\_BOOL</span></span>

<span data-ttu-id="04a72-110">**лвал**</span><span class="sxs-lookup"><span data-stu-id="04a72-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="04a72-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="04a72-111">Remarks</span></span>

<span data-ttu-id="04a72-112">Константа **мфнетсаурце \_ превиевмодинаблед** определяет идентификатор GUID для ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="04a72-112">The constant **MFNETSOURCE\_PREVIEWMODEENABLED** defines the GUID for the property key.</span></span> <span data-ttu-id="04a72-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="04a72-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="04a72-114">Это свойство задается в сетевом источнике путем передачи указателя **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="04a72-114">This property is set on the network source by passing an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="04a72-115">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="04a72-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="04a72-116">Требования</span><span class="sxs-lookup"><span data-stu-id="04a72-116">Requirements</span></span>



| <span data-ttu-id="04a72-117">Требование</span><span class="sxs-lookup"><span data-stu-id="04a72-117">Requirement</span></span> | <span data-ttu-id="04a72-118">Значение</span><span class="sxs-lookup"><span data-stu-id="04a72-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="04a72-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04a72-119">Minimum supported client</span></span><br/> | <span data-ttu-id="04a72-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="04a72-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="04a72-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04a72-121">Minimum supported server</span></span><br/> | <span data-ttu-id="04a72-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="04a72-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="04a72-123">Header</span><span class="sxs-lookup"><span data-stu-id="04a72-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="04a72-124"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="04a72-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04a72-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04a72-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04a72-126">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="04a72-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="04a72-127">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="04a72-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




