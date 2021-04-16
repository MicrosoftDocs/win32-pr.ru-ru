---
description: Метод DoAction объекта Session выполняет функцию действия, соответствующую указанному имени.
ms.assetid: 6cff1cf1-1c8f-4c43-a687-e927e8573e55
title: Метод Session. DoAction («фотополучение. h»)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.DoAction
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3084cfd51e7efbcfbfbc3cbcf2c9be21d8373d21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675723"
---
# <a name="sessiondoaction-method"></a><span data-ttu-id="785ae-103">Session. DoAction, метод</span><span class="sxs-lookup"><span data-stu-id="785ae-103">Session.DoAction method</span></span>

<span data-ttu-id="785ae-104">Метод **DoAction** объекта [**Session**](session-object.md) выполняет функцию действия, соответствующую указанному имени.</span><span class="sxs-lookup"><span data-stu-id="785ae-104">The **DoAction** method of the [**Session**](session-object.md) object executes the action function corresponding to the name supplied.</span></span> <span data-ttu-id="785ae-105">Если указано пустое имя действия, подсистема использует значение [свойства Action](action.md) в верхнем регистре в качестве выполняемого действия.</span><span class="sxs-lookup"><span data-stu-id="785ae-105">If a Null action name is supplied, the engine uses the uppercase value of the [ACTION property](action.md) as the action to perform.</span></span> <span data-ttu-id="785ae-106">Если значение свойства не определено, выполняется действие по умолчанию, которое в настоящее время определено как INSTALL.</span><span class="sxs-lookup"><span data-stu-id="785ae-106">If no property value is defined, the default action is performed, currently defined as INSTALL.</span></span> <span data-ttu-id="785ae-107">Этот метод возвращает целочисленное перечисление.</span><span class="sxs-lookup"><span data-stu-id="785ae-107">This method returns an integer enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="785ae-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="785ae-108">Syntax</span></span>


```JScript
Session.DoAction(
  action
)
```



## <a name="parameters"></a><span data-ttu-id="785ae-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="785ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="785ae-110">*action*</span><span class="sxs-lookup"><span data-stu-id="785ae-110">*action*</span></span> 
</dt> <dd>

<span data-ttu-id="785ae-111">Обязательное строковое имя действия, которое необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="785ae-111">Required string name of the action to execute.</span></span> <span data-ttu-id="785ae-112">С учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="785ae-112">Case-sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="785ae-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="785ae-113">Return value</span></span>

<span data-ttu-id="785ae-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="785ae-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="785ae-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="785ae-115">Remarks</span></span>

<span data-ttu-id="785ae-116">Действия, которые обновляют систему, такие как действия [инсталлфилес](installfiles-action.md) и [вритерегистривалуес](writeregistryvalues-action.md) , не могут быть запущены путем вызова метода **DoAction** .</span><span class="sxs-lookup"><span data-stu-id="785ae-116">Actions that update the system, such as the [InstallFiles](installfiles-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) actions, cannot be run by calling the **DoAction** method.</span></span> <span data-ttu-id="785ae-117">Исключением из этого правила является то, что метод **DoAction** вызывается из настраиваемого действия, запланированного в [таблице инсталлексекутесекуенце](installexecutesequence-table.md) между [действиями](installfinalize-action.md) [инсталлинитиализе](installinitialize-action.md) и функции InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="785ae-117">The exception to this rule is if the **DoAction** method is called from a custom action that is scheduled in the [InstallExecuteSequence table](installexecutesequence-table.md) between the [InstallInitialize](installinitialize-action.md) and [InstallFinalize actions](installfinalize-action.md).</span></span> <span data-ttu-id="785ae-118">Действия, которые не обновляют систему, например [аппсеарч](appsearch-action.md) или [костинитиализе](costinitialize-action.md), могут быть вызваны.</span><span class="sxs-lookup"><span data-stu-id="785ae-118">Actions that do not update the system, such as [AppSearch](appsearch-action.md) or [CostInitialize](costinitialize-action.md), can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="785ae-119">Требования</span><span class="sxs-lookup"><span data-stu-id="785ae-119">Requirements</span></span>



| <span data-ttu-id="785ae-120">Требование</span><span class="sxs-lookup"><span data-stu-id="785ae-120">Requirement</span></span> | <span data-ttu-id="785ae-121">Значение</span><span class="sxs-lookup"><span data-stu-id="785ae-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="785ae-122">Версия</span><span class="sxs-lookup"><span data-stu-id="785ae-122">Version</span></span><br/> | <span data-ttu-id="785ae-123">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="785ae-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="785ae-124">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="785ae-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="785ae-125">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="785ae-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="785ae-126">Header</span><span class="sxs-lookup"><span data-stu-id="785ae-126">Header</span></span><br/>  | <dl> <span data-ttu-id="785ae-127"><dt>Фотоприобретение. h</dt></span><span class="sxs-lookup"><span data-stu-id="785ae-127"><dt>Photoacquire.h</dt></span></span> </dl>                                                                                                                                                               |
| <span data-ttu-id="785ae-128">DLL</span><span class="sxs-lookup"><span data-stu-id="785ae-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="785ae-129"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="785ae-129"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="785ae-130">IID</span><span class="sxs-lookup"><span data-stu-id="785ae-130">IID</span></span><br/>     | <span data-ttu-id="785ae-131">IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="785ae-131">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




