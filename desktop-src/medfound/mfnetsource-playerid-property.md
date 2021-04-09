---
description: Значение \# поля &0034; c-плайерид&\# 0034;, используемое сетевым источником для ведения журнала.
ms.assetid: de52cc34-9b88-41ae-b8b8-ef5dff85892c
title: Свойство MFNETSOURCE_PLAYERID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d20754c93057ef3f000fc9c7201cda7ec287eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081168"
---
# <a name="mfnetsource_playerid-property"></a><span data-ttu-id="87218-103">МФНЕТСАУРЦЕ \_ плайерид, свойство</span><span class="sxs-lookup"><span data-stu-id="87218-103">MFNETSOURCE\_PLAYERID property</span></span>

<span data-ttu-id="87218-104">Значение поля "c-плайерид", используемое сетевым источником для ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="87218-104">The value of the "c-playerid" field that the network source uses for logging.</span></span> <span data-ttu-id="87218-105">Приложения могут задать для этого свойства любое строковое значение.</span><span class="sxs-lookup"><span data-stu-id="87218-105">Applications can set this property to any string value.</span></span>



<span data-ttu-id="87218-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="87218-106">Data type</span></span>

<span data-ttu-id="87218-107">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="87218-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="87218-108">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="87218-108">PROPVARIANT member</span></span>

<span data-ttu-id="87218-109">Строка расширенных символов (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="87218-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="87218-110">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="87218-110">VT\_LPWSTR</span></span>

<span data-ttu-id="87218-111">**пвсзвал**</span><span class="sxs-lookup"><span data-stu-id="87218-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="87218-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87218-112">Remarks</span></span>

<span data-ttu-id="87218-113">Константа **мфнетсаурце \_ плайерид** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="87218-113">The constant **MFNETSOURCE\_PLAYERID** defines the GUID for this property key.</span></span> <span data-ttu-id="87218-114">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="87218-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="87218-115">Приложения могут использовать это свойство для настройки сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="87218-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="87218-116">Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="87218-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="87218-117">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="87218-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="87218-118">Требования</span><span class="sxs-lookup"><span data-stu-id="87218-118">Requirements</span></span>



| <span data-ttu-id="87218-119">Требование</span><span class="sxs-lookup"><span data-stu-id="87218-119">Requirement</span></span> | <span data-ttu-id="87218-120">Значение</span><span class="sxs-lookup"><span data-stu-id="87218-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="87218-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87218-121">Minimum supported client</span></span><br/> | <span data-ttu-id="87218-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="87218-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="87218-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87218-123">Minimum supported server</span></span><br/> | <span data-ttu-id="87218-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="87218-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="87218-125">Header</span><span class="sxs-lookup"><span data-stu-id="87218-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="87218-126"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="87218-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87218-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87218-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87218-128">Ведение журнала клиента</span><span class="sxs-lookup"><span data-stu-id="87218-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="87218-129">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="87218-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="87218-130">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="87218-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




