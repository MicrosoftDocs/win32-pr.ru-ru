---
description: Метод Сетинсталллевел объекта Session устанавливает для текущей установки уровень установки в указанное значение и повторно вычисляет состояние SELECT и установленные состояния для всех компонентов в таблице Feature.
ms.assetid: d47f8025-d484-42c7-9808-5ee590a4d200
title: Session. Сетинсталллевел, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SetInstallLevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: abb5ff5f7a528ff654787e9b2ee3d935abee57d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652244"
---
# <a name="sessionsetinstalllevel-method"></a><span data-ttu-id="3573b-103">Session. Сетинсталллевел, метод</span><span class="sxs-lookup"><span data-stu-id="3573b-103">Session.SetInstallLevel method</span></span>

<span data-ttu-id="3573b-104">Метод **сетинсталллевел** объекта [**Session**](session-object.md) устанавливает для текущей установки уровень установки в указанное значение и повторно вычисляет состояние SELECT и установленные состояния для всех компонентов в таблице Feature.</span><span class="sxs-lookup"><span data-stu-id="3573b-104">The **SetInstallLevel** method of the [**Session**](session-object.md) object sets the install level for the current installation to a specified value and recalculates the Select and Installed states for all features in the Feature table.</span></span> <span data-ttu-id="3573b-105">Он также задает состояние действия каждого компонента в [таблице Component](component-table.md) на основе нового уровня.</span><span class="sxs-lookup"><span data-stu-id="3573b-105">It also sets the Action state of each component in the [Component table](component-table.md) based on the new level.</span></span>

## <a name="syntax"></a><span data-ttu-id="3573b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3573b-106">Syntax</span></span>


```JScript
Session.SetInstallLevel(
  installLevel
)
```



## <a name="parameters"></a><span data-ttu-id="3573b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3573b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3573b-108">*инсталллевел*</span><span class="sxs-lookup"><span data-stu-id="3573b-108">*installLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="3573b-109">Требуется запрошенный новый уровень установки.</span><span class="sxs-lookup"><span data-stu-id="3573b-109">Required requested new install level.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3573b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3573b-110">Return value</span></span>

<span data-ttu-id="3573b-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3573b-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3573b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3573b-112">Remarks</span></span>

<span data-ttu-id="3573b-113">Перед вызовом **сетинсталллевел** необходимо выполнить [действие костинитиализе](costinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="3573b-113">The [CostInitialize action](costinitialize-action.md) must be executed prior to calling **SetInstallLevel**.</span></span>

<span data-ttu-id="3573b-114">Если для параметра *инсталллевел* передано значение 0, текущий уровень установки не изменяется, но все компоненты по-прежнему обновляются на основе текущего уровня установки.</span><span class="sxs-lookup"><span data-stu-id="3573b-114">If 0 is passed for the *installLevel* parameter, the current install level is not changed, but all features are still updated based on the current install level.</span></span> <span data-ttu-id="3573b-115">Например, эта функция может использоваться модулем обработчика для сброса всех выбранных значений в начальном состоянии по умолчанию в любой момент в процессе выбора пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3573b-115">For example, this functionality could be used by the Handler module to reset all selections back to their initial default states at any point in the UI selection process.</span></span>

<span data-ttu-id="3573b-116">В случае сбоя метода можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="3573b-116">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3573b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3573b-117">Requirements</span></span>



| <span data-ttu-id="3573b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3573b-118">Requirement</span></span> | <span data-ttu-id="3573b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3573b-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3573b-120">Версия</span><span class="sxs-lookup"><span data-stu-id="3573b-120">Version</span></span><br/> | <span data-ttu-id="3573b-121">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3573b-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3573b-122">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3573b-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3573b-123">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="3573b-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3573b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3573b-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="3573b-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3573b-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3573b-126">IID</span><span class="sxs-lookup"><span data-stu-id="3573b-126">IID</span></span><br/>     | <span data-ttu-id="3573b-127">IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3573b-127">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




