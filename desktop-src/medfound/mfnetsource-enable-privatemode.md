---
description: Включает частный режим загрузки в сетевом источнике.
ms.assetid: 679661A7-1D31-43F3-A64E-16ADCB5414B0
title: Свойство MFNETSOURCE_ENABLE_PRIVATEMODE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53aa0bde3bf76ded278e0e3ee37465adb717972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711269"
---
# <a name="mfnetsource_enable_privatemode-property"></a><span data-ttu-id="2448b-103">МФНЕТСАУРЦЕ \_ включить \_ свойство приватемоде</span><span class="sxs-lookup"><span data-stu-id="2448b-103">MFNETSOURCE\_ENABLE\_PRIVATEMODE property</span></span>

<span data-ttu-id="2448b-104">Включает частный режим загрузки в сетевом источнике.</span><span class="sxs-lookup"><span data-stu-id="2448b-104">Enables private download mode in the network source.</span></span>



<span data-ttu-id="2448b-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2448b-105">Data type</span></span>

<span data-ttu-id="2448b-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="2448b-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="2448b-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="2448b-107">PROPVARIANT member</span></span>

<span data-ttu-id="2448b-108">**ЛОГИЧЕСКОМ**</span><span class="sxs-lookup"><span data-stu-id="2448b-108">**BOOL**</span></span>

<span data-ttu-id="2448b-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="2448b-109">VT\_I4</span></span>

<span data-ttu-id="2448b-110">**лвал**</span><span class="sxs-lookup"><span data-stu-id="2448b-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="2448b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2448b-111">Remarks</span></span>

<span data-ttu-id="2448b-112">Если это свойство имеет **значение true**, кэш удаляется после завершения сеанса.</span><span class="sxs-lookup"><span data-stu-id="2448b-112">If this property is **TRUE**, the cache is cleared when the session ends.</span></span>

<span data-ttu-id="2448b-113">Константа **\_ клиентгуид мфнетсаурце** определяет идентификатор GUID для ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="2448b-113">The **MFNETSOURCE\_CLIENTGUID** constant defines the GUID for the property key.</span></span> <span data-ttu-id="2448b-114">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="2448b-114">The property identifier (PID) is zero.</span></span> <span data-ttu-id="2448b-115">Чтобы задать это свойство в сетевом источнике, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="2448b-115">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="2448b-116">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="2448b-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2448b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2448b-117">Requirements</span></span>



| <span data-ttu-id="2448b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2448b-118">Requirement</span></span> | <span data-ttu-id="2448b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2448b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2448b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2448b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2448b-121">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2448b-121">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2448b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2448b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2448b-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2448b-123">None supported</span></span><br/>                                                          |
| <span data-ttu-id="2448b-124">Header</span><span class="sxs-lookup"><span data-stu-id="2448b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2448b-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2448b-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2448b-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2448b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2448b-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2448b-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="2448b-128">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2448b-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




