---
description: Метод размер файла объекта Installer использует вызовы API Win32 для получения размера файла, указанного в параметре Path.
ms.assetid: d7119e5e-9315-4b20-a904-bc1104f3a4e4
title: Метод Installer. Размер файла
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 593319b88e3942ae6caa1399adbe2e596bf6e737
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651605"
---
# <a name="installerfilesize-method"></a><span data-ttu-id="0c945-103">Метод Installer. Размер файла</span><span class="sxs-lookup"><span data-stu-id="0c945-103">Installer.FileSize method</span></span>

<span data-ttu-id="0c945-104">Метод **Размер файла** объекта [**Installer**](installer-object.md) использует вызовы API Win32 для получения размера файла, указанного в параметре *path*.</span><span class="sxs-lookup"><span data-stu-id="0c945-104">The **FileSize** method of the [**Installer**](installer-object.md) object uses Win32 API calls to return the size of the file specified in *Path*.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c945-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c945-105">Syntax</span></span>


```JScript
Installer.FileSize(
  Path
)
```



## <a name="parameters"></a><span data-ttu-id="0c945-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c945-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c945-107">*Путь*</span><span class="sxs-lookup"><span data-stu-id="0c945-107">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="0c945-108">Обязательная строка, содержащая путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="0c945-108">Required string containing the path to the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c945-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c945-109">Return value</span></span>

<span data-ttu-id="0c945-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0c945-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c945-111">Требования</span><span class="sxs-lookup"><span data-stu-id="0c945-111">Requirements</span></span>



| <span data-ttu-id="0c945-112">Требование</span><span class="sxs-lookup"><span data-stu-id="0c945-112">Requirement</span></span> | <span data-ttu-id="0c945-113">Значение</span><span class="sxs-lookup"><span data-stu-id="0c945-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c945-114">Версия</span><span class="sxs-lookup"><span data-stu-id="0c945-114">Version</span></span><br/> | <span data-ttu-id="0c945-115">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0c945-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0c945-116">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0c945-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0c945-117">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c945-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0c945-118">DLL</span><span class="sxs-lookup"><span data-stu-id="0c945-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="0c945-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c945-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0c945-120">IID</span><span class="sxs-lookup"><span data-stu-id="0c945-120">IID</span></span><br/>     | <span data-ttu-id="0c945-121">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0c945-121">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




