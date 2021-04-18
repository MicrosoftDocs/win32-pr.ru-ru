---
description: Перечисление наборов символов BLOB-объектов указывает кодировку, \_ \_ используемую текущим объектом-blobом для конференций.
ms.assetid: 79131b84-19b5-492b-a44e-9d47c365b298
title: Перечисление BLOB_CHARACTER_SET (Сдпблб. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b180a8574f1643a5fc1be134be99c951faaf1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675717"
---
# <a name="blob_character_set-enumeration"></a><span data-ttu-id="990c4-103">\_Перечисление наборов символов BLOB-объектов \_</span><span class="sxs-lookup"><span data-stu-id="990c4-103">BLOB\_CHARACTER\_SET enumeration</span></span>

<span data-ttu-id="990c4-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="990c4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="990c4-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="990c4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="990c4-106">Перечисление **\_ \_ наборов символов BLOB-объектов** указывает кодировку, используемую текущим объектом-blobом для конференций.</span><span class="sxs-lookup"><span data-stu-id="990c4-106">The **BLOB\_CHARACTER\_SET** enum indicates the character set used by the current conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="990c4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="990c4-107">Syntax</span></span>


```C++
} BLOB_CHARACTER_SET;
```



## <a name="constants"></a><span data-ttu-id="990c4-108">Константы</span><span class="sxs-lookup"><span data-stu-id="990c4-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="990c4-109"><span id="BCS_ASCII"></span><span id="bcs_ascii"></span>**код \_ ASCII для BCS**</span><span class="sxs-lookup"><span data-stu-id="990c4-109"><span id="BCS_ASCII"></span><span id="bcs_ascii"></span>**BCS\_ASCII**</span></span>
</dt> <dd>

<span data-ttu-id="990c4-110">Стандартный формат ASCII.</span><span class="sxs-lookup"><span data-stu-id="990c4-110">Standard ASCII format.</span></span>

</dd> <dt>

<span data-ttu-id="990c4-111"><span id="BCS_UTF7"></span><span id="bcs_utf7"></span>**\_UTF7 BCS**</span><span class="sxs-lookup"><span data-stu-id="990c4-111"><span id="BCS_UTF7"></span><span id="bcs_utf7"></span>**BCS\_UTF7**</span></span>
</dt> <dd>

<span data-ttu-id="990c4-112">Семь-разрядный формат преобразования Юникода.</span><span class="sxs-lookup"><span data-stu-id="990c4-112">Seven-bit transformation format of Unicode.</span></span> <span data-ttu-id="990c4-113">Для получения дополнительных сведений об этом формате выполните поиск в Интернете по RFC 1642.</span><span class="sxs-lookup"><span data-stu-id="990c4-113">For details on this format, conduct an Internet search for RFC 1642.</span></span>

</dd> <dt>

<span data-ttu-id="990c4-114"><span id="BCS_UTF8"></span><span id="bcs_utf8"></span>**Синхронизация BCS (в \_ UTF8)**</span><span class="sxs-lookup"><span data-stu-id="990c4-114"><span id="BCS_UTF8"></span><span id="bcs_utf8"></span>**BCS\_UTF8**</span></span>
</dt> <dd>

<span data-ttu-id="990c4-115">Формат преобразования UCS 8.</span><span class="sxs-lookup"><span data-stu-id="990c4-115">UCS Transformation Format 8.</span></span> <span data-ttu-id="990c4-116">Чтобы получить подробные сведения об этом формате, выполните поиск в Интернете для ISO (Международная организация по стандартизации) и IEC (IEC) документа ISO/IEC JTC1/SC2/WG2 N 1036, датированный 1, 1994, в редакторе проектов WG2.</span><span class="sxs-lookup"><span data-stu-id="990c4-116">For details on this format, conduct an Internet search for ISO (the International Organization for Standardization) and IEC (the International Electrotechnical Commission) document ISO/IEC JTC1/SC2/WG2 N 1036, dated August 1, 1994, by WG2 Project Editor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="990c4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="990c4-117">Requirements</span></span>



| <span data-ttu-id="990c4-118">Требование</span><span class="sxs-lookup"><span data-stu-id="990c4-118">Requirement</span></span> | <span data-ttu-id="990c4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="990c4-119">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="990c4-120">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="990c4-120">TAPI version</span></span><br/> | <span data-ttu-id="990c4-121">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="990c4-121">Requires TAPI 3.0 or later</span></span><br/>                                               |
| <span data-ttu-id="990c4-122">Header</span><span class="sxs-lookup"><span data-stu-id="990c4-122">Header</span></span><br/>       | <dl> <span data-ttu-id="990c4-123"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="990c4-123"><dt>Sdpblb.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="990c4-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="990c4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="990c4-125">**итдиректорйобжектконференце**</span><span class="sxs-lookup"><span data-stu-id="990c4-125">**ITDirectoryObjectConference**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> <dt>

[<span data-ttu-id="990c4-126">**получить \_ кодировку**</span><span class="sxs-lookup"><span data-stu-id="990c4-126">**get\_CharacterSet**</span></span>](itconferenceblob-get-characterset.md)
</dt> <dt>

[<span data-ttu-id="990c4-127">**Ini**</span><span class="sxs-lookup"><span data-stu-id="990c4-127">**Init**</span></span>](itconferenceblob-init.md)
</dt> <dt>

[<span data-ttu-id="990c4-128">**сетконференцеблоб**</span><span class="sxs-lookup"><span data-stu-id="990c4-128">**SetConferenceBlob**</span></span>](itconferenceblob-setconferenceblob.md)
</dt> </dl>

 

 




