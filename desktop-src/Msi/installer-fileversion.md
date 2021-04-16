---
description: Метод FileVersion объекта Installer возвращает строку версии или строку языка пути, указанного в параметре path, используя формат, в котором установщик планирует найти их в базе данных.
ms.assetid: 387cf269-5a7a-476b-811e-d576da1c752f
title: Метод Installer. FileVersion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileVersion
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a36a92b42815a1b2df913ba6bd9f687cdd1b609b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651604"
---
# <a name="installerfileversion-method"></a><span data-ttu-id="cfa50-103">Метод Installer. FileVersion</span><span class="sxs-lookup"><span data-stu-id="cfa50-103">Installer.FileVersion method</span></span>

<span data-ttu-id="cfa50-104">Метод **FileVersion** объекта [**Installer**](installer-object.md) возвращает строку версии или строку языка пути, указанного в параметре *path* , используя формат, в котором установщик планирует найти их в базе данных.</span><span class="sxs-lookup"><span data-stu-id="cfa50-104">The **FileVersion** method of the [**Installer**](installer-object.md) object returns the version string or language string of the path specified in *Path* using the format in which the installer expects to find them in the database.</span></span> <span data-ttu-id="cfa50-105">Для версий это строка в \# формате ". \# . \# . \# ".</span><span class="sxs-lookup"><span data-stu-id="cfa50-105">For versions, this is a string in "\#.\#.\#.\#" format.</span></span> <span data-ttu-id="cfa50-106">Для языка это Десятичный идентификатор языка.</span><span class="sxs-lookup"><span data-stu-id="cfa50-106">For language, this is the decimal language ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfa50-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cfa50-107">Syntax</span></span>


```JScript
Installer.FileVersion(
  Path,
  Language
)
```



## <a name="parameters"></a><span data-ttu-id="cfa50-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cfa50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfa50-109">*Путь*</span><span class="sxs-lookup"><span data-stu-id="cfa50-109">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="cfa50-110">Обязательная строка, содержащая путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="cfa50-110">Required string containing the path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="cfa50-111">*Язык*</span><span class="sxs-lookup"><span data-stu-id="cfa50-111">*Language*</span></span> 
</dt> <dd>

<span data-ttu-id="cfa50-112">Флаг, определяющий, является ли возвращаемое значение ИДЕНТИФИКАТОРом языка или строкой версии.</span><span class="sxs-lookup"><span data-stu-id="cfa50-112">Flag for designating whether the returned value is a language ID or version string.</span></span> <span data-ttu-id="cfa50-113">TRUE Возвращает язык, FALSE Возвращает версию.</span><span class="sxs-lookup"><span data-stu-id="cfa50-113">TRUE returns the language, FALSE returns the version.</span></span> <span data-ttu-id="cfa50-114">Этот параметр является необязательным и имеет значение по умолчанию FALSE.</span><span class="sxs-lookup"><span data-stu-id="cfa50-114">This parameter is optional, with a default value of FALSE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfa50-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cfa50-115">Return value</span></span>

<span data-ttu-id="cfa50-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cfa50-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfa50-117">Требования</span><span class="sxs-lookup"><span data-stu-id="cfa50-117">Requirements</span></span>



| <span data-ttu-id="cfa50-118">Требование</span><span class="sxs-lookup"><span data-stu-id="cfa50-118">Requirement</span></span> | <span data-ttu-id="cfa50-119">Значение</span><span class="sxs-lookup"><span data-stu-id="cfa50-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfa50-120">Версия</span><span class="sxs-lookup"><span data-stu-id="cfa50-120">Version</span></span><br/> | <span data-ttu-id="cfa50-121">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cfa50-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cfa50-122">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cfa50-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cfa50-123">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="cfa50-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="cfa50-124">DLL</span><span class="sxs-lookup"><span data-stu-id="cfa50-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="cfa50-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfa50-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="cfa50-126">IID</span><span class="sxs-lookup"><span data-stu-id="cfa50-126">IID</span></span><br/>     | <span data-ttu-id="cfa50-127">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="cfa50-127">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




