---
description: Метод Коллектусеринфо объекта Installer вызывает последовательность мастера пользовательского интерфейса, которая собирает и сохраняет сведения о пользователе и код продукта.
ms.assetid: 2faacf38-1af1-4e8a-a3f6-87733104614e
title: Метод Installer. Коллектусеринфо
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CollectUserInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d7286fdbc9fab6b3db6752284bf86db05f920bd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651968"
---
# <a name="installercollectuserinfo-method"></a><span data-ttu-id="6142d-103">Метод Installer. Коллектусеринфо</span><span class="sxs-lookup"><span data-stu-id="6142d-103">Installer.CollectUserInfo method</span></span>

<span data-ttu-id="6142d-104">Метод **коллектусеринфо** объекта [**Installer**](installer-object.md) вызывает последовательность мастера пользовательского интерфейса, которая собирает и сохраняет сведения о пользователе и код продукта.</span><span class="sxs-lookup"><span data-stu-id="6142d-104">The **CollectUserInfo** method of the [**Installer**](installer-object.md) object invokes a user interface wizard sequence which collects and stores both user information and the product code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6142d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6142d-105">Syntax</span></span>


```JScript
Installer.CollectUserInfo(
  Product
)
```



## <a name="parameters"></a><span data-ttu-id="6142d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6142d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6142d-107">*Продукт*</span><span class="sxs-lookup"><span data-stu-id="6142d-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="6142d-108">Указывает [**код продукта**](productcode.md) .</span><span class="sxs-lookup"><span data-stu-id="6142d-108">Specifies the [**product code**](productcode.md) of the product.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6142d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6142d-109">Return value</span></span>

<span data-ttu-id="6142d-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6142d-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6142d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6142d-111">Remarks</span></span>

<span data-ttu-id="6142d-112">Приложение должно вызывать метод **коллектусеринфо** при первом запуске.</span><span class="sxs-lookup"><span data-stu-id="6142d-112">An application should call the **CollectUserInfo** method the first time it is run.</span></span> <span data-ttu-id="6142d-113">Метод **коллектусеринфо** открывает пакет установки продукта и вызывает последовательность мастера созданного пользовательского интерфейса, который собирает сведения о пользователе.</span><span class="sxs-lookup"><span data-stu-id="6142d-113">The **CollectUserInfo** method opens the product's installation package and invokes an authored user interface wizard sequence which collects user information.</span></span> <span data-ttu-id="6142d-114">После завершения последовательности мастера регистрируется собранная информация о пользователе.</span><span class="sxs-lookup"><span data-stu-id="6142d-114">Upon completion of the wizard sequence, the collected user information is registered.</span></span> <span data-ttu-id="6142d-115">Свойству [**duilevel**](installer-uilevel.md) должно быть присвоено значение мсиуилевелфулл, так как этот API требует созданного пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6142d-115">The [**UILevel**](installer-uilevel.md) property should be set to msiUILevelFull because this API requires an authored user interface.</span></span>

<span data-ttu-id="6142d-116">Метод **коллектусеринфо** вызывает [диалоговое окно файла firstrun](firstrun-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="6142d-116">The **CollectUserInfo** method invokes the [FirstRun Dialog](firstrun-dialog.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6142d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6142d-117">Requirements</span></span>



| <span data-ttu-id="6142d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6142d-118">Requirement</span></span> | <span data-ttu-id="6142d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6142d-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6142d-120">Версия</span><span class="sxs-lookup"><span data-stu-id="6142d-120">Version</span></span><br/> | <span data-ttu-id="6142d-121">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6142d-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6142d-122">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6142d-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6142d-123">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="6142d-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="6142d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6142d-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="6142d-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6142d-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="6142d-126">IID</span><span class="sxs-lookup"><span data-stu-id="6142d-126">IID</span></span><br/>     | <span data-ttu-id="6142d-127">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="6142d-127">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="6142d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6142d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6142d-129">**мсиколлектусеринфо**</span><span class="sxs-lookup"><span data-stu-id="6142d-129">**MsiCollectUserInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
</dt> </dl>

 

 




