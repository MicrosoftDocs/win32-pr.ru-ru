---
description: Массив строк с параметрами для отправки на сервер журнала.
ms.assetid: 36d711c7-a1ff-4ef2-b633-5f9f1662801e
title: Свойство MFNETSOURCE_LOGPARAMS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec30f3f4d85f44905288601ba73ee6c246d8a9db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991471"
---
# <a name="mfnetsource_logparams-property"></a><span data-ttu-id="884c1-103">МФНЕТСАУРЦЕ \_ логпарамс, свойство</span><span class="sxs-lookup"><span data-stu-id="884c1-103">MFNETSOURCE\_LOGPARAMS property</span></span>

<span data-ttu-id="884c1-104">Массив строк с параметрами для отправки на сервер журнала.</span><span class="sxs-lookup"><span data-stu-id="884c1-104">Array of strings with the parameters to send to the log server.</span></span>



<span data-ttu-id="884c1-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="884c1-105">Data type</span></span>

<span data-ttu-id="884c1-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="884c1-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="884c1-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="884c1-107">PROPVARIANT member</span></span>

<span data-ttu-id="884c1-108">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="884c1-108">\**WCHAR\** _</span></span>

<span data-ttu-id="884c1-109">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="884c1-109">VT\_LPWSTR</span></span>

<span data-ttu-id="884c1-110">_ *пвсзвал*\*</span><span class="sxs-lookup"><span data-stu-id="884c1-110">_ *pwszVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="884c1-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="884c1-111">Remarks</span></span>

<span data-ttu-id="884c1-112">Константа **\_ логпарамс мфнетсаурце** определяет идентификатор GUID для ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="884c1-112">The **MFNETSOURCE\_LOGPARAMS** constant defines the GUID for the property key.</span></span> <span data-ttu-id="884c1-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="884c1-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="884c1-114">Чтобы задать это свойство в сетевом источнике, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="884c1-114">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="884c1-115">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="884c1-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="884c1-116">Требования</span><span class="sxs-lookup"><span data-stu-id="884c1-116">Requirements</span></span>



| <span data-ttu-id="884c1-117">Требование</span><span class="sxs-lookup"><span data-stu-id="884c1-117">Requirement</span></span> | <span data-ttu-id="884c1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="884c1-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="884c1-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="884c1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="884c1-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="884c1-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="884c1-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="884c1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="884c1-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="884c1-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="884c1-123">Header</span><span class="sxs-lookup"><span data-stu-id="884c1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="884c1-124"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="884c1-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="884c1-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="884c1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="884c1-126">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="884c1-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="884c1-127">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="884c1-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




