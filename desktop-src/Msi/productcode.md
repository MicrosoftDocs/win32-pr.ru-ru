---
description: Свойство ProductCode — это уникальный идентификатор для конкретного выпуска продукта, представленный в виде строкового GUID, например &\# 0034; {12345678-1234-1234-1234-123456789012}&\# 0034;.
ms.assetid: 33cedd37-0343-471c-ad4b-0db5f98d5894
title: ProductCode, свойство
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a714687ab49bca07d1137b3395cb19ddba0944
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675974"
---
# <a name="productcode-property"></a><span data-ttu-id="c9c47-103">ProductCode, свойство</span><span class="sxs-lookup"><span data-stu-id="c9c47-103">ProductCode property</span></span>

<span data-ttu-id="c9c47-104">Свойство **ProductCode** — это уникальный идентификатор для конкретного выпуска продукта, представленный в виде строкового [GUID](guid.md), например " {12345678-1234-1234-1234-123456789012} ".</span><span class="sxs-lookup"><span data-stu-id="c9c47-104">The **ProductCode** property is a unique identifier for the particular product release, represented as a string [GUID](guid.md), for example "{12345678-1234-1234-1234-123456789012}".</span></span> <span data-ttu-id="c9c47-105">Буквы, используемые в этом GUID, должны быть прописными буквами.</span><span class="sxs-lookup"><span data-stu-id="c9c47-105">Letters used in this GUID must be uppercase.</span></span> <span data-ttu-id="c9c47-106">Этот идентификатор должен различаться для разных версий и языков.</span><span class="sxs-lookup"><span data-stu-id="c9c47-106">This ID must vary for different versions and languages.</span></span>

<span data-ttu-id="c9c47-107">Обновление продукта, которое обновляет продукт в совершенно новом продукте, также должно изменить код продукта.</span><span class="sxs-lookup"><span data-stu-id="c9c47-107">A product upgrade that updates a product into an entirely new product must also change the product code.</span></span> <span data-ttu-id="c9c47-108">В 32-разрядных и 64-разрядных версиях пакета приложения должны быть назначены разные коды продуктов.</span><span class="sxs-lookup"><span data-stu-id="c9c47-108">The 32-bit and 64-bit versions of an application's package must be assigned different product codes.</span></span>

<span data-ttu-id="c9c47-109">**Код продукта** объявляется как свойство продукта, и является основным методом указания продукта.</span><span class="sxs-lookup"><span data-stu-id="c9c47-109">The **ProductCode** is advertised as a product property, and is the primary method of specifying the product.</span></span> <span data-ttu-id="c9c47-110">Это свойство является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c9c47-110">This property is REQUIRED.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9c47-111">Требования</span><span class="sxs-lookup"><span data-stu-id="c9c47-111">Requirements</span></span>



| <span data-ttu-id="c9c47-112">Требование</span><span class="sxs-lookup"><span data-stu-id="c9c47-112">Requirement</span></span> | <span data-ttu-id="c9c47-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c9c47-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9c47-114">Версия</span><span class="sxs-lookup"><span data-stu-id="c9c47-114">Version</span></span><br/> | <span data-ttu-id="c9c47-115">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c9c47-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c9c47-116">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c9c47-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c9c47-117">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c9c47-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c9c47-118">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="c9c47-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c9c47-119">См. также</span><span class="sxs-lookup"><span data-stu-id="c9c47-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9c47-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="c9c47-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




