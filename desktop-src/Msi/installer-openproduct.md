---
description: Метод Опенпродукт объекта Installer открывает пакет установщика для установленного продукта с помощью кода продукта и возвращает объект Session.
ms.assetid: f09c4795-19e1-4474-b7ca-68ef650b69d5
title: Метод Installer. Опенпродукт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9fd25a1f204a6d42cd4cb6e330d7d69da2cddb07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652171"
---
# <a name="installeropenproduct-method"></a><span data-ttu-id="5fd0e-103">Метод Installer. Опенпродукт</span><span class="sxs-lookup"><span data-stu-id="5fd0e-103">Installer.OpenProduct method</span></span>

<span data-ttu-id="5fd0e-104">Метод **опенпродукт** объекта [**Installer**](installer-object.md) открывает пакет установщика для установленного продукта с помощью кода продукта и возвращает объект [**Session**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="5fd0e-104">The **OpenProduct** method of the [**Installer**](installer-object.md) object opens an installer package for an installed product using the product code and returns a [**Session**](session-object.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fd0e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5fd0e-105">Syntax</span></span>


```JScript
Installer.OpenProduct(
  productCode
)
```



## <a name="parameters"></a><span data-ttu-id="5fd0e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5fd0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fd0e-107">*productCode*</span><span class="sxs-lookup"><span data-stu-id="5fd0e-107">*productCode*</span></span> 
</dt> <dd>

<span data-ttu-id="5fd0e-108">Обязательная строка, содержащая уникальный код продукта ( [GUID](guid.md)) или дескриптор активации, написанный установщиком.</span><span class="sxs-lookup"><span data-stu-id="5fd0e-108">Required string containing the unique product code (a [GUID](guid.md)) or an activation descriptor written by the installer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fd0e-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5fd0e-109">Return value</span></span>

<span data-ttu-id="5fd0e-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5fd0e-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fd0e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5fd0e-111">Remarks</span></span>

<span data-ttu-id="5fd0e-112">Обратите внимание, что один процесс может открыть только один объект [**сеанса**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="5fd0e-112">Note that only one [**Session**](session-object.md) object can be opened by a single process.</span></span> <span data-ttu-id="5fd0e-113">**Опенпродукт** нельзя использовать в настраиваемом действии, поскольку активная установка является единственным разрешенным сеансом.</span><span class="sxs-lookup"><span data-stu-id="5fd0e-113">**OpenProduct** cannot be used in a custom action because the active installation is the only session allowed.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fd0e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="5fd0e-114">Requirements</span></span>



| <span data-ttu-id="5fd0e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="5fd0e-115">Requirement</span></span> | <span data-ttu-id="5fd0e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5fd0e-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fd0e-117">Версия</span><span class="sxs-lookup"><span data-stu-id="5fd0e-117">Version</span></span><br/> | <span data-ttu-id="5fd0e-118">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5fd0e-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5fd0e-119">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5fd0e-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5fd0e-120">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="5fd0e-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5fd0e-121">DLL</span><span class="sxs-lookup"><span data-stu-id="5fd0e-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="5fd0e-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fd0e-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5fd0e-123">IID</span><span class="sxs-lookup"><span data-stu-id="5fd0e-123">IID</span></span><br/>     | <span data-ttu-id="5fd0e-124">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5fd0e-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




