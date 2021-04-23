---
description: Значение \# поля &0034; c-хостексе&\# 0034;, используемое сетевым источником для ведения журнала.
ms.assetid: 82a49719-b9b3-4868-bbcf-9e376f35d4c4
title: Свойство MFNETSOURCE_HOSTEXE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ac786fe08ede556537703d2eb886b30be39207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817121"
---
# <a name="mfnetsource_hostexe-property"></a><span data-ttu-id="b4788-103">МФНЕТСАУРЦЕ \_ хостексе, свойство</span><span class="sxs-lookup"><span data-stu-id="b4788-103">MFNETSOURCE\_HOSTEXE property</span></span>

<span data-ttu-id="b4788-104">Значение поля "c-хостексе", используемое сетевым источником для ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="b4788-104">The value of the "c-hostexe" field that the network source uses for logging.</span></span> <span data-ttu-id="b4788-105">Приложения могут задать для этого свойства имя ведущего приложения.</span><span class="sxs-lookup"><span data-stu-id="b4788-105">Applications can set this property to the name of the host application.</span></span> <span data-ttu-id="b4788-106">Например, значение может быть "iexplore.exe", если приложение размещено на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="b4788-106">For example, the value could be "iexplore.exe" if the application is hosted in a webpage.</span></span>



<span data-ttu-id="b4788-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b4788-107">Data type</span></span>

<span data-ttu-id="b4788-108">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="b4788-108">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="b4788-109">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="b4788-109">PROPVARIANT member</span></span>

<span data-ttu-id="b4788-110">Строка расширенных символов (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="b4788-110">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="b4788-111">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="b4788-111">VT\_LPWSTR</span></span>

<span data-ttu-id="b4788-112">**пвсзвал**</span><span class="sxs-lookup"><span data-stu-id="b4788-112">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="b4788-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4788-113">Remarks</span></span>

<span data-ttu-id="b4788-114">Константа **мфнетсаурце \_ хостексе** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="b4788-114">The constant **MFNETSOURCE\_HOSTEXE** defines the GUID for this property key.</span></span> <span data-ttu-id="b4788-115">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="b4788-115">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="b4788-116">Приложения могут использовать это свойство для настройки сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="b4788-116">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="b4788-117">Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="b4788-117">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="b4788-118">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="b4788-118">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4788-119">Требования</span><span class="sxs-lookup"><span data-stu-id="b4788-119">Requirements</span></span>



| <span data-ttu-id="b4788-120">Требование</span><span class="sxs-lookup"><span data-stu-id="b4788-120">Requirement</span></span> | <span data-ttu-id="b4788-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b4788-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b4788-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4788-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b4788-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b4788-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b4788-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4788-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b4788-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b4788-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b4788-126">Header</span><span class="sxs-lookup"><span data-stu-id="b4788-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4788-127"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4788-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4788-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4788-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4788-129">Ведение журнала клиента</span><span class="sxs-lookup"><span data-stu-id="b4788-129">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="b4788-130">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b4788-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="b4788-131">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b4788-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




