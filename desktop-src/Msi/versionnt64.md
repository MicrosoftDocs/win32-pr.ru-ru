---
description: Установщик задает для свойства VersionNT64 номер версии операционной системы, только если система работает на 64-разрядном компьютере.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: VersionNT64, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3b1b5a26b2ba45b859b6330bf153300e239074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675317"
---
# <a name="versionnt64-property"></a><span data-ttu-id="c3743-103">VersionNT64, свойство</span><span class="sxs-lookup"><span data-stu-id="c3743-103">VersionNT64 property</span></span>

<span data-ttu-id="c3743-104">Установщик задает для свойства **VersionNT64** номер версии операционной системы, только если система работает на 64-разрядном компьютере.</span><span class="sxs-lookup"><span data-stu-id="c3743-104">The installer sets the **VersionNT64** property to the version number for the operating system only if the system is running on a 64-bit computer.</span></span> <span data-ttu-id="c3743-105">Если операционная система не является 64-разрядной, свойство не определено.</span><span class="sxs-lookup"><span data-stu-id="c3743-105">The property is undefined if the operating system is not 64-bit.</span></span>

<span data-ttu-id="c3743-106">Значение является целым числом: MajorVersion \* 100 + minorversion.</span><span class="sxs-lookup"><span data-stu-id="c3743-106">The value is an integer: MajorVersion \* 100 + MinorVersion.</span></span>

<span data-ttu-id="c3743-107">По соображениям совместимости свойство также не определено, если свойство [**сводки шаблона**](template-summary.md) указывает, что пакет предназначен для 32-разрядных систем Intel, а операционная система является 64-разрядной архитектурой, не Intel64 или x64 (например, ARM64).</span><span class="sxs-lookup"><span data-stu-id="c3743-107">For compatibility reasons, the property is also undefined if the [**Template Summary**](template-summary.md) property indicates the package is for 32-bit Intel systems and the operating system is a 64-bit architecture that is not Intel64 or x64 (such as ARM64).</span></span>

## <a name="remarks"></a><span data-ttu-id="c3743-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c3743-108">Remarks</span></span>

<span data-ttu-id="c3743-109">Проверка условных выражений на 64-разрядную версию Windows осуществляется просто с помощью имени свойства или путем проверки версии с помощью оператора сравнения.</span><span class="sxs-lookup"><span data-stu-id="c3743-109">Conditional expressions test for 64-bit Windows simply by using the property name, or by verifying the version using a comparison operator.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3743-110">Требования</span><span class="sxs-lookup"><span data-stu-id="c3743-110">Requirements</span></span>



| <span data-ttu-id="c3743-111">Требование</span><span class="sxs-lookup"><span data-stu-id="c3743-111">Requirement</span></span> | <span data-ttu-id="c3743-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c3743-112">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3743-113">Версия</span><span class="sxs-lookup"><span data-stu-id="c3743-113">Version</span></span><br/> | <span data-ttu-id="c3743-114">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c3743-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c3743-115">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c3743-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c3743-116">Установщик Windows в Windows Server 2003 или Windows XP ознакомьтесь с [требованиями к установщик Windows Run-Time](windows-installer-portal.md) , чтобы получить сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии.</span><span class="sxs-lookup"><span data-stu-id="c3743-116">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c3743-117">См. также</span><span class="sxs-lookup"><span data-stu-id="c3743-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3743-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="c3743-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 




