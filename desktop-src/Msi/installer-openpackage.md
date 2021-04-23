---
description: Метод Опенпаккаже объекта Installer открывает пакет установщика для использования с функциями, которые обращаются к базе данных продукта и подсистеме установки, возвращая объект Session.
ms.assetid: 22b03bde-29ae-4dd4-a41c-d55b3a4f424c
title: Метод Installer. Опенпаккаже
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenPackage
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 621fac51155b2ac89eba40d39da6d5af6c305e67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651595"
---
# <a name="installeropenpackage-method"></a><span data-ttu-id="0f613-103">Метод Installer. Опенпаккаже</span><span class="sxs-lookup"><span data-stu-id="0f613-103">Installer.OpenPackage method</span></span>

<span data-ttu-id="0f613-104">Метод **опенпаккаже** объекта [**Installer**](installer-object.md) открывает пакет установщика для использования с функциями, которые обращаются к базе данных продукта и подсистеме установки, возвращая объект [**Session**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="0f613-104">The **OpenPackage** method of the [**Installer**](installer-object.md) object opens an installer package for use with functions that access the product database and install engine, returning an [**Session**](session-object.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f613-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f613-105">Syntax</span></span>


```JScript
Installer.OpenPackage(
  packagePath,
  options
)
```



## <a name="parameters"></a><span data-ttu-id="0f613-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f613-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f613-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="0f613-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="0f613-108">Обязательная строка, содержащая имя пути пакета.</span><span class="sxs-lookup"><span data-stu-id="0f613-108">Required string containing the path name of the package.</span></span>

</dd> <dt>

<span data-ttu-id="0f613-109">*options*</span><span class="sxs-lookup"><span data-stu-id="0f613-109">*options*</span></span> 
</dt> <dd>

<span data-ttu-id="0f613-110">Необязательное целочисленное значение, указывающее, должно ли **опенпаккаже** игнорировать текущее состояние компьютера при создании объекта Session.</span><span class="sxs-lookup"><span data-stu-id="0f613-110">An optional integer value that specifies whether or not **OpenPackage** should ignore the current computer state when creating the Session object.</span></span> <span data-ttu-id="0f613-111">Если значение параметра не равно 0, то параметру по умолчанию будет присвоено исходное поведение.</span><span class="sxs-lookup"><span data-stu-id="0f613-111">No value or a value of 0 for options defaults to the original behavior.</span></span> <span data-ttu-id="0f613-112">Если параметр имеет значение 1, метод **опенпаккаже** игнорирует текущее состояние компьютера при открытии пакета.</span><span class="sxs-lookup"><span data-stu-id="0f613-112">When options is 1, the **OpenPackage** Method ignores the current computer state when opening the package.</span></span> <span data-ttu-id="0f613-113">Значение 1 предотвращает изменение текущего состояния компьютера.</span><span class="sxs-lookup"><span data-stu-id="0f613-113">A value of 1 prevents changes to the current computer state.</span></span> <span data-ttu-id="0f613-114">Дополнительные сведения см. в разделе [**мсиопенпаккажеекс**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span><span class="sxs-lookup"><span data-stu-id="0f613-114">For more information, see [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f613-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f613-115">Return value</span></span>

<span data-ttu-id="0f613-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0f613-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f613-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f613-117">Remarks</span></span>

<span data-ttu-id="0f613-118">Метод **опенпаккаже** может принять обработчик базы данных непосредственно вместо строки для пути пакета.</span><span class="sxs-lookup"><span data-stu-id="0f613-118">The **OpenPackage** method can accept the database handle directly instead of the string for the package path.</span></span>

<span data-ttu-id="0f613-119">Обратите внимание, что один процесс может открыть только один объект [**сеанса**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="0f613-119">Note that only one [**Session**](session-object.md) object can be opened by a single process.</span></span> <span data-ttu-id="0f613-120">**Опенпаккаже** нельзя использовать в настраиваемом действии, поскольку активная установка является единственным разрешенным сеансом.</span><span class="sxs-lookup"><span data-stu-id="0f613-120">**OpenPackage** cannot be used in a custom action because the active installation is the only session allowed.</span></span>

<span data-ttu-id="0f613-121">Объект безопасного [**сеанса**](session-object.md) пропускает текущее состояние компьютера при открытии пакета и предотвращает изменения в текущем состоянии компьютера.</span><span class="sxs-lookup"><span data-stu-id="0f613-121">A safe [**Session**](session-object.md) object ignores the current computer state when opening the package and prevents changes to the current computer state.</span></span> <span data-ttu-id="0f613-122">Дополнительные сведения см. в разделе [**мсиопенпаккажеекс**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span><span class="sxs-lookup"><span data-stu-id="0f613-122">For more information, see [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f613-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0f613-123">Requirements</span></span>



| <span data-ttu-id="0f613-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0f613-124">Requirement</span></span> | <span data-ttu-id="0f613-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0f613-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f613-126">Версия</span><span class="sxs-lookup"><span data-stu-id="0f613-126">Version</span></span><br/> | <span data-ttu-id="0f613-127">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0f613-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0f613-128">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0f613-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0f613-129">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="0f613-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0f613-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0f613-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="0f613-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f613-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0f613-132">IID</span><span class="sxs-lookup"><span data-stu-id="0f613-132">IID</span></span><br/>     | <span data-ttu-id="0f613-133">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0f613-133">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




