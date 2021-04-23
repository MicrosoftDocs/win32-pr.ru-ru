---
description: Метод Екстрактпатчксмлдата объекта Installer извлекает сведения из исправления в виде XML-строки. Эти сведения можно использовать для определения того, применяется ли исправление к целевой системе. Этот метод вызывает Мсиекстрактпатчксмлдата.
ms.assetid: 85940940-2002-4cb1-8e29-ba2374bf3796
title: Метод Installer. Екстрактпатчксмлдата
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ExtractPatchXMLData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 69c17236c0a4cd96820e0366df51b28cf47ecfb0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651624"
---
# <a name="installerextractpatchxmldata-method"></a><span data-ttu-id="cd595-105">Метод Installer. Екстрактпатчксмлдата</span><span class="sxs-lookup"><span data-stu-id="cd595-105">Installer.ExtractPatchXMLData method</span></span>

<span data-ttu-id="cd595-106">Метод **екстрактпатчксмлдата** объекта [**Installer**](installer-object.md) извлекает сведения из исправления в виде XML-строки.</span><span class="sxs-lookup"><span data-stu-id="cd595-106">The **ExtractPatchXMLData** method of the [**Installer**](installer-object.md) object extracts information from a patch as an XML string.</span></span> <span data-ttu-id="cd595-107">Эти сведения можно использовать для определения того, применяется ли исправление к целевой системе.</span><span class="sxs-lookup"><span data-stu-id="cd595-107">The information can be used to determine whether the patch applies on a target system.</span></span> <span data-ttu-id="cd595-108">Этот метод вызывает [**мсиекстрактпатчксмлдата**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span><span class="sxs-lookup"><span data-stu-id="cd595-108">This method calls [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span></span>

## <a name="syntax"></a><span data-ttu-id="cd595-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd595-109">Syntax</span></span>


```JScript
Installer.ExtractPatchXMLData(
  PatchPath
)
```



## <a name="parameters"></a><span data-ttu-id="cd595-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd595-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd595-111">*патчпас*</span><span class="sxs-lookup"><span data-stu-id="cd595-111">*PatchPath*</span></span> 
</dt> <dd>

<span data-ttu-id="cd595-112">Полный путь к исправлению, из которого извлекаются сведения о применимости.</span><span class="sxs-lookup"><span data-stu-id="cd595-112">Full path to the patch from which the applicability information is to be extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd595-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd595-113">Return value</span></span>

<span data-ttu-id="cd595-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cd595-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd595-115">Требования</span><span class="sxs-lookup"><span data-stu-id="cd595-115">Requirements</span></span>



| <span data-ttu-id="cd595-116">Требование</span><span class="sxs-lookup"><span data-stu-id="cd595-116">Requirement</span></span> | <span data-ttu-id="cd595-117">Значение</span><span class="sxs-lookup"><span data-stu-id="cd595-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd595-118">Версия</span><span class="sxs-lookup"><span data-stu-id="cd595-118">Version</span></span><br/> | <span data-ttu-id="cd595-119">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cd595-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cd595-120">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cd595-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cd595-121">Установщик Windows 3,0 или более поздней версии в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cd595-121">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="cd595-122">DLL</span><span class="sxs-lookup"><span data-stu-id="cd595-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="cd595-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd595-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="cd595-124">IID</span><span class="sxs-lookup"><span data-stu-id="cd595-124">IID</span></span><br/>     | <span data-ttu-id="cd595-125">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="cd595-125">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="cd595-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd595-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd595-127">**мсиекстрактпатчксмлдата**</span><span class="sxs-lookup"><span data-stu-id="cd595-127">**MsiExtractPatchXMLData**</span></span>](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> <dt>

[<span data-ttu-id="cd595-128">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="cd595-128">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




