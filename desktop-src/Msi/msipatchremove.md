---
description: Свойство МСИПАТЧРЕМОВЕ указывает список исправлений, удаляемых во время установки.
ms.assetid: 76f8daa9-d32c-4845-85bc-52b728f53d1f
title: МСИПАТЧРЕМОВЕ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf83583c5b15311e175e67a867ff5aca71394b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665383"
---
# <a name="msipatchremove-property"></a><span data-ttu-id="7c20a-103">МСИПАТЧРЕМОВЕ, свойство</span><span class="sxs-lookup"><span data-stu-id="7c20a-103">MSIPATCHREMOVE property</span></span>

<span data-ttu-id="7c20a-104">Свойство **мсипатчремове** указывает список исправлений, удаляемых во время установки.</span><span class="sxs-lookup"><span data-stu-id="7c20a-104">The **MSIPATCHREMOVE** property specifies the list of patches to remove during an installation.</span></span> <span data-ttu-id="7c20a-105">Отдельные исправления в списке разделяются точками с запятой. их можно представить с помощью GUID кода исправления или полного пути к исправлению.</span><span class="sxs-lookup"><span data-stu-id="7c20a-105">Individual patches in the list are separated by semicolons and can be represented by patch code GUID or the full path to the patch.</span></span> <span data-ttu-id="7c20a-106">Функция [**мсиремовепатчес**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) и метод [**ремовепатчес**](installer-removepatches.md) объекта [Installer](installer-object.md) задают свойство **мсипатчремове** .</span><span class="sxs-lookup"><span data-stu-id="7c20a-106">The [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) function and the [**RemovePatches**](installer-removepatches.md) method of the [Installer](installer-object.md) object set the **MSIPATCHREMOVE** property.</span></span>

<span data-ttu-id="7c20a-107">Свойство **мсипатчремове** может быть задано в командной строке следующим образом для удаления исправления.</span><span class="sxs-lookup"><span data-stu-id="7c20a-107">The **MSIPATCHREMOVE** property can be set on the command line as follows to remove a patch.</span></span>

<span data-ttu-id="7c20a-108">**msiexec/i A: \\Example.msi мсипатчремове = c: \\ патчи \\ qfe1. MSP; { 0BBB87F1-3186-409C-8CDD-C88AA2A4A7E0}; {A86B443B-E3BF-4009-ADED-F716FC735858}/QB**</span><span class="sxs-lookup"><span data-stu-id="7c20a-108">**msiexec /i A:\\Example.msi MSIPATCHREMOVE=c:\\patches\\qfe1.msp;{0BBB87F1-3186-409C-8CDD-C88AA2A4A7E0};{A86B443B-E3BF-4009-ADED-F716FC735858}/qb**</span></span>

## <a name="requirements"></a><span data-ttu-id="7c20a-109">Требования</span><span class="sxs-lookup"><span data-stu-id="7c20a-109">Requirements</span></span>



| <span data-ttu-id="7c20a-110">Требование</span><span class="sxs-lookup"><span data-stu-id="7c20a-110">Requirement</span></span> | <span data-ttu-id="7c20a-111">Значение</span><span class="sxs-lookup"><span data-stu-id="7c20a-111">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c20a-112">Версия</span><span class="sxs-lookup"><span data-stu-id="7c20a-112">Version</span></span><br/> | <span data-ttu-id="7c20a-113">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7c20a-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7c20a-114">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7c20a-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7c20a-115">Установщик Windows 3,0 или более поздней версии в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7c20a-115">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="7c20a-116">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="7c20a-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7c20a-117">См. также</span><span class="sxs-lookup"><span data-stu-id="7c20a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c20a-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="7c20a-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="7c20a-119">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="7c20a-119">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




