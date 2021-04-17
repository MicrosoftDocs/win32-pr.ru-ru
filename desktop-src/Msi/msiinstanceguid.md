---
description: Наличие свойства МСИИНСТАНЦЕГУИД указывает, что код продукта&\# 8211; изменение преобразования зарегистрировано для продукта.
ms.assetid: c39be15d-e10a-4055-bd81-aa7510a19fe4
title: МСИИНСТАНЦЕГУИД, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c798d56cf3ede6a75a133dd7e0ec7f42c32e84f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675020"
---
# <a name="msiinstanceguid-property"></a><span data-ttu-id="06ea4-103">МСИИНСТАНЦЕГУИД, свойство</span><span class="sxs-lookup"><span data-stu-id="06ea4-103">MSIINSTANCEGUID property</span></span>

<span data-ttu-id="06ea4-104">Наличие свойства **мсиинстанцегуид** указывает, что код продукта — изменение преобразования регистрируется для продукта.</span><span class="sxs-lookup"><span data-stu-id="06ea4-104">The presence of the **MSIINSTANCEGUID** property indicates that a product code–changing transform is registered to the product.</span></span> <span data-ttu-id="06ea4-105">Значение свойства **мсиинстанцегуид** указывает, какой экземпляр продукта следует использовать для установки.</span><span class="sxs-lookup"><span data-stu-id="06ea4-105">The value of the **MSIINSTANCEGUID** property specifies which instance of a product is to be used for installation.</span></span> <span data-ttu-id="06ea4-106">Свойство **мсиинстанцегуид** может ссылаться только на продукт, который уже был установлен с преобразованием экземпляра.</span><span class="sxs-lookup"><span data-stu-id="06ea4-106">The **MSIINSTANCEGUID** property can only reference a product that has already been installed with an instance transform.</span></span>

<span data-ttu-id="06ea4-107">Преобразования экземпляров — это код продукта — изменение преобразований, доступных для установщика, работающего в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="06ea4-107">Instance transforms are product code–changing transforms available with the installer running on either Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="06ea4-108">Дополнительные сведения см. в разделе [Установка нескольких экземпляров продуктов и исправлений](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="06ea4-108">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="06ea4-109">Требования</span><span class="sxs-lookup"><span data-stu-id="06ea4-109">Requirements</span></span>



| <span data-ttu-id="06ea4-110">Требование</span><span class="sxs-lookup"><span data-stu-id="06ea4-110">Requirement</span></span> | <span data-ttu-id="06ea4-111">Значение</span><span class="sxs-lookup"><span data-stu-id="06ea4-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06ea4-112">Версия</span><span class="sxs-lookup"><span data-stu-id="06ea4-112">Version</span></span><br/> | <span data-ttu-id="06ea4-113">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="06ea4-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="06ea4-114">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="06ea4-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="06ea4-115">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="06ea4-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="06ea4-116">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="06ea4-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06ea4-117">См. также</span><span class="sxs-lookup"><span data-stu-id="06ea4-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06ea4-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="06ea4-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="06ea4-119">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="06ea4-119">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




