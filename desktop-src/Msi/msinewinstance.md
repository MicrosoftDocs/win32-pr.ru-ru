---
description: Свойство МСИНЕВИНСТАНЦЕ указывает установку нового экземпляра продукта с преобразованиями экземпляра.
ms.assetid: 35d41fa9-79d3-4baa-b177-5a32239b5051
title: МСИНЕВИНСТАНЦЕ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8b51ec02d7b30c42e6e400b6a6177d7ef47d88c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668874"
---
# <a name="msinewinstance-property"></a><span data-ttu-id="370c6-103">МСИНЕВИНСТАНЦЕ, свойство</span><span class="sxs-lookup"><span data-stu-id="370c6-103">MSINEWINSTANCE property</span></span>

<span data-ttu-id="370c6-104">Свойство **мсиневинстанце** указывает установку нового экземпляра продукта с преобразованиями экземпляра.</span><span class="sxs-lookup"><span data-stu-id="370c6-104">The **MSINEWINSTANCE** property indicates the installation of a new instance of a product with instance transforms.</span></span> <span data-ttu-id="370c6-105">Это свойство поддерживает несколько экземпляров с помощью кода продукта — изменение преобразований.</span><span class="sxs-lookup"><span data-stu-id="370c6-105">This property supports multiple instances through product code–changing transforms.</span></span> <span data-ttu-id="370c6-106">Значение этого свойства равно 1.</span><span class="sxs-lookup"><span data-stu-id="370c6-106">The value of this property is 1.</span></span> <span data-ttu-id="370c6-107">Наличие этого свойства в командной строке требует наличия также свойства [**TRANSFORMS**](transforms.md) .</span><span class="sxs-lookup"><span data-stu-id="370c6-107">The presence of this property on the command line requires that the [**TRANSFORMS**](transforms.md) property also be present.</span></span> <span data-ttu-id="370c6-108">Первое преобразование, перечисленное в **ПРЕобразованиях** , должно быть преобразованием экземпляра.</span><span class="sxs-lookup"><span data-stu-id="370c6-108">The first transform listed in **TRANSFORMS** must be an instance transform.</span></span> <span data-ttu-id="370c6-109">Дополнительные сведения см. в разделе [Установка нескольких экземпляров продуктов и исправлений](installing-multiple-instances-of-products-and-patches.md) .</span><span class="sxs-lookup"><span data-stu-id="370c6-109">For more information see, [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md)</span></span>

<span data-ttu-id="370c6-110">Это свойство доступно в установщике, работающем под управлением системы Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="370c6-110">This property is available with the installer running a system in the Windows Server 2003 or Windows XP.</span></span>

## <a name="requirements"></a><span data-ttu-id="370c6-111">Требования</span><span class="sxs-lookup"><span data-stu-id="370c6-111">Requirements</span></span>



| <span data-ttu-id="370c6-112">Требование</span><span class="sxs-lookup"><span data-stu-id="370c6-112">Requirement</span></span> | <span data-ttu-id="370c6-113">Значение</span><span class="sxs-lookup"><span data-stu-id="370c6-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="370c6-114">Версия</span><span class="sxs-lookup"><span data-stu-id="370c6-114">Version</span></span><br/> | <span data-ttu-id="370c6-115">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="370c6-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="370c6-116">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="370c6-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="370c6-117">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="370c6-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="370c6-118">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="370c6-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="370c6-119">См. также</span><span class="sxs-lookup"><span data-stu-id="370c6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="370c6-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="370c6-120">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="370c6-121">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="370c6-121">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




