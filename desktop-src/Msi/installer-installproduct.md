---
description: Метод Инсталлпродукт объекта Installer открывает пакет установщика и инициализирует сеанс установки.
ms.assetid: 6828ca34-3cf1-4738-882d-9ff1450f1014
title: Метод Installer. Инсталлпродукт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.InstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 08bab1081aae186b40494cff777163679847b44b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651600"
---
# <a name="installerinstallproduct-method"></a><span data-ttu-id="3535b-103">Метод Installer. Инсталлпродукт</span><span class="sxs-lookup"><span data-stu-id="3535b-103">Installer.InstallProduct method</span></span>

<span data-ttu-id="3535b-104">Метод **инсталлпродукт** объекта [**Installer**](installer-object.md) открывает пакет установщика и инициализирует сеанс установки.</span><span class="sxs-lookup"><span data-stu-id="3535b-104">The **InstallProduct** method of the [**Installer**](installer-object.md) object opens an installer package and initializes an install session.</span></span>

## <a name="syntax"></a><span data-ttu-id="3535b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3535b-105">Syntax</span></span>


```JScript
Installer.InstallProduct(
  packagePath,
  propertyValues
)
```



## <a name="parameters"></a><span data-ttu-id="3535b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3535b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3535b-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="3535b-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="3535b-108">Обязательная строка, содержащая путь к установочному пакету.</span><span class="sxs-lookup"><span data-stu-id="3535b-108">Required string containing the path to the install package.</span></span>

</dd> <dt>

<span data-ttu-id="3535b-109">*propertyValues*</span><span class="sxs-lookup"><span data-stu-id="3535b-109">*propertyValues*</span></span> 
</dt> <dd>

<span data-ttu-id="3535b-110">Необязательная строка, содержащая пары "свойство = значение", разделенные пробелом.</span><span class="sxs-lookup"><span data-stu-id="3535b-110">Optional string containing property=value pairs separated by white space.</span></span>

<span data-ttu-id="3535b-111">Чтобы выполнить административную установку, включите ACTION = ADMIN в *пропертивалуес*.</span><span class="sxs-lookup"><span data-stu-id="3535b-111">To perform an administrative installation, include ACTION=ADMIN in *propertyValues*.</span></span> <span data-ttu-id="3535b-112">Дополнительные сведения см. в описании свойства [**Action**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="3535b-112">For more information, see the [**ACTION**](action.md) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3535b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3535b-113">Return value</span></span>

<span data-ttu-id="3535b-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3535b-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3535b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3535b-115">Remarks</span></span>

<span data-ttu-id="3535b-116">Чтобы полностью удалить продукт, задайте Remove = ALL в *пропертивалуес*.</span><span class="sxs-lookup"><span data-stu-id="3535b-116">To completely remove a product, set REMOVE=ALL in *propertyValues*.</span></span> <span data-ttu-id="3535b-117">Дополнительные сведения см. в разделе [**Remove**](remove.md) Property.</span><span class="sxs-lookup"><span data-stu-id="3535b-117">For more information, see [**REMOVE**](remove.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="3535b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="3535b-118">Requirements</span></span>



| <span data-ttu-id="3535b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="3535b-119">Requirement</span></span> | <span data-ttu-id="3535b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="3535b-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3535b-121">Версия</span><span class="sxs-lookup"><span data-stu-id="3535b-121">Version</span></span><br/> | <span data-ttu-id="3535b-122">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3535b-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3535b-123">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3535b-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3535b-124">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="3535b-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3535b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3535b-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="3535b-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3535b-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3535b-127">IID</span><span class="sxs-lookup"><span data-stu-id="3535b-127">IID</span></span><br/>     | <span data-ttu-id="3535b-128">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3535b-128">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




