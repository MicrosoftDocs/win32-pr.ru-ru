---
description: Установщик задает для свойства VersionNT64 номер версии операционной системы, только если система работает на 64-разрядном компьютере.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: VersionNT64, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f6c0f2037891527f17feba92d7e9c8494aa622
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262076"
---
# <a name="versionnt64-property"></a><span data-ttu-id="0999c-103">VersionNT64, свойство</span><span class="sxs-lookup"><span data-stu-id="0999c-103">VersionNT64 property</span></span>

<span data-ttu-id="0999c-104">Установщик задает для свойства **VersionNT64** номер версии операционной системы, только если система работает на 64-разрядном компьютере.</span><span class="sxs-lookup"><span data-stu-id="0999c-104">The installer sets the **VersionNT64** property to the version number for the operating system only if the system is running on a 64-bit computer.</span></span> <span data-ttu-id="0999c-105">Если операционная система не является 64-разрядной, свойство не определено.</span><span class="sxs-lookup"><span data-stu-id="0999c-105">The property is undefined if the operating system is not 64-bit.</span></span>

<span data-ttu-id="0999c-106">Значение является целым числом: MajorVersion \* 100 + minorversion.</span><span class="sxs-lookup"><span data-stu-id="0999c-106">The value is an integer: MajorVersion \* 100 + MinorVersion.</span></span>

<span data-ttu-id="0999c-107">По соображениям совместимости свойство также не определено, если свойство [**сводки шаблона**](template-summary.md) указывает, что пакет предназначен для 32-разрядных систем Intel (x86), а операционная система не может запустить 64-разрядный код Intel (x64), например Windows 10 в ARM (ARM64).</span><span class="sxs-lookup"><span data-stu-id="0999c-107">For compatibility reasons, the property is also undefined if the [**Template Summary**](template-summary.md) property indicates the package is for 32-bit Intel (x86) systems and the operating system cannot run 64-bit Intel (x64) code, such as Windows 10 on ARM (ARM64).</span></span>

> [!NOTE]
> <span data-ttu-id="0999c-108">Начиная с Windows 10 Build 21277, сборки ARM64 в канале разработки программы предварительной оценки Windows имеют поддержку для 64-разрядных приложений.</span><span class="sxs-lookup"><span data-stu-id="0999c-108">As of Windows 10 Build 21277, ARM64 builds in the Dev channel of the Windows Insider Preview program have support for x64 applications.</span></span> <span data-ttu-id="0999c-109">Для этих сборок ARM64 свойство VersionNT64 определено для пакетов x86.</span><span class="sxs-lookup"><span data-stu-id="0999c-109">On these ARM64 builds, the VersionNT64 property is defined for x86 packages.</span></span>

## <a name="remarks"></a><span data-ttu-id="0999c-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="0999c-110">Remarks</span></span>

<span data-ttu-id="0999c-111">Проверка условных выражений на 64-разрядную версию Windows осуществляется просто с помощью имени свойства или путем проверки версии с помощью оператора сравнения.</span><span class="sxs-lookup"><span data-stu-id="0999c-111">Conditional expressions test for 64-bit Windows simply by using the property name, or by verifying the version using a comparison operator.</span></span>

## <a name="requirements"></a><span data-ttu-id="0999c-112">Требования</span><span class="sxs-lookup"><span data-stu-id="0999c-112">Requirements</span></span>



| <span data-ttu-id="0999c-113">Требование</span><span class="sxs-lookup"><span data-stu-id="0999c-113">Requirement</span></span> | <span data-ttu-id="0999c-114">Значение</span><span class="sxs-lookup"><span data-stu-id="0999c-114">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0999c-115">Version</span><span class="sxs-lookup"><span data-stu-id="0999c-115">Version</span></span><br/> | <span data-ttu-id="0999c-116">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0999c-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0999c-117">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0999c-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0999c-118">Установщик Windows в Windows Server 2003 или Windows XP ознакомьтесь с [требованиями к установщик Windows Run-Time](windows-installer-portal.md) , чтобы получить сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии.</span><span class="sxs-lookup"><span data-stu-id="0999c-118">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0999c-119">См. также</span><span class="sxs-lookup"><span data-stu-id="0999c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0999c-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="0999c-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




