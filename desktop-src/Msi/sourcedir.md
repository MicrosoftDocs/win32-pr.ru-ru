---
description: Свойство SourceDir — это корневой каталог, содержащий исходный CAB-файл или дерево исходного файла пакета установки. Это значение используется для разрешения каталога.
ms.assetid: 900b26e8-80dd-4e70-8d79-37f09a0c6e86
title: SourceDir, свойство
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a366e4afecdd16722a06ecfbec08552baab8f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679858"
---
# <a name="sourcedir-property"></a><span data-ttu-id="90af2-104">SourceDir, свойство</span><span class="sxs-lookup"><span data-stu-id="90af2-104">SourceDir property</span></span>

<span data-ttu-id="90af2-105">Свойство **SourceDir** — это корневой каталог, содержащий исходный CAB-файл или дерево исходного файла пакета установки.</span><span class="sxs-lookup"><span data-stu-id="90af2-105">The **SourceDir** property is the root directory that contains the source cabinet file or the source file tree of the installation package.</span></span> <span data-ttu-id="90af2-106">Это значение используется для разрешения каталога.</span><span class="sxs-lookup"><span data-stu-id="90af2-106">This value is used for directory resolution.</span></span>

## <a name="default-value"></a><span data-ttu-id="90af2-107">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="90af2-107">Default Value</span></span>

<span data-ttu-id="90af2-108">Каталог, содержащий пакет установки.</span><span class="sxs-lookup"><span data-stu-id="90af2-108">The directory that contains the installation package.</span></span>

## <a name="remarks"></a><span data-ttu-id="90af2-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90af2-109">Remarks</span></span>

<span data-ttu-id="90af2-110">[Действие ресолвесаурце](resolvesource-action.md) должно быть вызвано перед использованием свойства **SourceDir** в любом выражении или при попытке получить значение **SourceDir** с [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span><span class="sxs-lookup"><span data-stu-id="90af2-110">The [ResolveSource action](resolvesource-action.md) must be called before using the **SourceDir** property in any expression or attempting to retrieve the value of **SourceDir** with [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span></span> <span data-ttu-id="90af2-111">Действие Ресолвесаурце не должно выполняться, пока источник недоступен, например, при удалении приложения, так как это может привести к непреднамеренному появлению запроса к исходному носителю.</span><span class="sxs-lookup"><span data-stu-id="90af2-111">The ResolveSource action should not be run while the source is unavailable, such as when uninstalling an application, because this can cause an unintended prompt for the source media.</span></span>

## <a name="requirements"></a><span data-ttu-id="90af2-112">Требования</span><span class="sxs-lookup"><span data-stu-id="90af2-112">Requirements</span></span>



| <span data-ttu-id="90af2-113">Требование</span><span class="sxs-lookup"><span data-stu-id="90af2-113">Requirement</span></span> | <span data-ttu-id="90af2-114">Значение</span><span class="sxs-lookup"><span data-stu-id="90af2-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90af2-115">Версия</span><span class="sxs-lookup"><span data-stu-id="90af2-115">Version</span></span><br/> | <span data-ttu-id="90af2-116">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="90af2-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="90af2-117">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="90af2-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="90af2-118">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="90af2-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="90af2-119">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="90af2-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="90af2-120">См. также</span><span class="sxs-lookup"><span data-stu-id="90af2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90af2-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="90af2-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




