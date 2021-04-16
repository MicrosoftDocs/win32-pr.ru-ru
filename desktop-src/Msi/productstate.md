---
description: Установщик задает для свойства Продуктстате состояние установки продукта при инициализации.
ms.assetid: 833e9a15-10f8-4b1c-945f-bc02b506f627
title: Продуктстате, свойство
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51ea88058aa8bae6b67acaea96b506a7560c7a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680120"
---
# <a name="productstate-property"></a><span data-ttu-id="29625-103">Продуктстате, свойство</span><span class="sxs-lookup"><span data-stu-id="29625-103">ProductState property</span></span>

<span data-ttu-id="29625-104">Установщик задает для свойства **продуктстате** состояние установки продукта при инициализации.</span><span class="sxs-lookup"><span data-stu-id="29625-104">The installer sets the **ProductState** property to the installation state for the product at initialization.</span></span> <span data-ttu-id="29625-105">Для этого свойства задан один из следующих типов данных INSTALLSTATE, возвращаемых [**мсикуерипродуктстате**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea).</span><span class="sxs-lookup"><span data-stu-id="29625-105">This property is set to one of the following INSTALLSTATE data types returned by [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea).</span></span>



| <span data-ttu-id="29625-106">INSTALLSTATE</span><span class="sxs-lookup"><span data-stu-id="29625-106">INSTALLSTATE</span></span>             | <span data-ttu-id="29625-107">Числовое значение</span><span class="sxs-lookup"><span data-stu-id="29625-107">Numeric value</span></span> | <span data-ttu-id="29625-108">Состояние установки продукта</span><span class="sxs-lookup"><span data-stu-id="29625-108">Installation state of product</span></span>                   |
|--------------------------|---------------|-------------------------------------------------|
| <span data-ttu-id="29625-109">INSTALLSTATE \_ неизвестный</span><span class="sxs-lookup"><span data-stu-id="29625-109">INSTALLSTATE\_UNKNOWN</span></span>    | <span data-ttu-id="29625-110">-1</span><span class="sxs-lookup"><span data-stu-id="29625-110">-1</span></span>            | <span data-ttu-id="29625-111">Продукт не объявлен или не установлен.</span><span class="sxs-lookup"><span data-stu-id="29625-111">The product is neither advertised or installed.</span></span> |
| <span data-ttu-id="29625-112">INSTALLSTATE \_ объявлено</span><span class="sxs-lookup"><span data-stu-id="29625-112">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="29625-113">1</span><span class="sxs-lookup"><span data-stu-id="29625-113">1</span></span>             | <span data-ttu-id="29625-114">Продукт объявлен, но не установлен.</span><span class="sxs-lookup"><span data-stu-id="29625-114">The product is advertised but not installed.</span></span>    |
| <span data-ttu-id="29625-115">\_отсутствует InstallState</span><span class="sxs-lookup"><span data-stu-id="29625-115">INSTALLSTATE\_ABSENT</span></span>     | <span data-ttu-id="29625-116">2</span><span class="sxs-lookup"><span data-stu-id="29625-116">2</span></span>             | <span data-ttu-id="29625-117">Продукт устанавливается для другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="29625-117">The product is installed for a different user.</span></span>  |
| <span data-ttu-id="29625-118">INSTALLSTATE \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="29625-118">INSTALLSTATE\_DEFAULT</span></span>    | <span data-ttu-id="29625-119">5</span><span class="sxs-lookup"><span data-stu-id="29625-119">5</span></span>             | <span data-ttu-id="29625-120">Продукт установлен для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="29625-120">The product is installed for the current user.</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="29625-121">Требования</span><span class="sxs-lookup"><span data-stu-id="29625-121">Requirements</span></span>



| <span data-ttu-id="29625-122">Требование</span><span class="sxs-lookup"><span data-stu-id="29625-122">Requirement</span></span> | <span data-ttu-id="29625-123">Значение</span><span class="sxs-lookup"><span data-stu-id="29625-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29625-124">Версия</span><span class="sxs-lookup"><span data-stu-id="29625-124">Version</span></span><br/> | <span data-ttu-id="29625-125">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="29625-125">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="29625-126">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="29625-126">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="29625-127">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="29625-127">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="29625-128">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="29625-128">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="29625-129">См. также</span><span class="sxs-lookup"><span data-stu-id="29625-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29625-130">Свойства</span><span class="sxs-lookup"><span data-stu-id="29625-130">Properties</span></span>](properties.md)
</dt> </dl>

 

 




