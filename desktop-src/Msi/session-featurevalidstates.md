---
description: Свойство Феатуревалидстатес объекта Session возвращает целое число, представляющее битовые флаги с каждым соответствующим битом, представляющим допустимое состояние установки для указанного компонента.
ms.assetid: 8a1f6911-b0a6-4fac-ba77-df4f1b7d15e2
title: Свойство Session. Феатуревалидстатес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureValidStates
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b76080bb7854c75cbfbb06697de9fc7d7a1af0c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652098"
---
# <a name="sessionfeaturevalidstates-property"></a><span data-ttu-id="471c3-103">Свойство Session. Феатуревалидстатес</span><span class="sxs-lookup"><span data-stu-id="471c3-103">Session.FeatureValidStates property</span></span>

<span data-ttu-id="471c3-104">Свойство **феатуревалидстатес** объекта [**Session**](session-object.md) возвращает целое число, представляющее битовые флаги с каждым соответствующим битом, представляющим допустимое состояние установки для указанного компонента.</span><span class="sxs-lookup"><span data-stu-id="471c3-104">The **FeatureValidStates** property of the [**Session**](session-object.md) object returns an integer representing bit flags with each relevant bit representing a valid installation state for the specified feature.</span></span>

<span data-ttu-id="471c3-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="471c3-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="471c3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="471c3-106">Syntax</span></span>


```JScript
propVal = Session.FeatureValidStates
```



## <a name="property-value"></a><span data-ttu-id="471c3-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="471c3-107">Property value</span></span>

<span data-ttu-id="471c3-108">Обязательное строковое имя элемента компонента, для которого должны быть получены допустимые состояния установки.</span><span class="sxs-lookup"><span data-stu-id="471c3-108">Required string name of the feature item whose valid installation states are to be retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="471c3-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="471c3-109">Remarks</span></span>

<span data-ttu-id="471c3-110">Возвращаемое значение состоит из битовых флагов, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="471c3-110">The return value is composed of bit flags as follows.</span></span> <span data-ttu-id="471c3-111">Бит 0. Если задано, local является допустимым состоянием.</span><span class="sxs-lookup"><span data-stu-id="471c3-111">Bit 0: if set, Local is a valid state.</span></span> <span data-ttu-id="471c3-112">Бит 1. Если задано, источник является допустимым состоянием.</span><span class="sxs-lookup"><span data-stu-id="471c3-112">Bit 1: if set, Source is a valid state.</span></span>

<span data-ttu-id="471c3-113">Свойство **феатуревалидстатес** успешно работает только после того, как установщик вызывал действия [костинитиализе](costinitialize-action.md) и [костфинализе](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="471c3-113">The **FeatureValidStates** property only succeeds after the installer has called the [CostInitialize](costinitialize-action.md) and [CostFinalize](costfinalize-action.md) actions.</span></span>

<span data-ttu-id="471c3-114">**Феатуревалидстатес** определяет срок действия состояния, запрашивая все компоненты, связанные с указанным компонентом, без учета текущего установленного состояния любого компонента.</span><span class="sxs-lookup"><span data-stu-id="471c3-114">**FeatureValidStates** determines state validity by querying all components that are linked to the specified feature without taking into account the current installed state of any component.</span></span>

<span data-ttu-id="471c3-115">Возможные допустимые состояния для функции определяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="471c3-115">The possible valid states for a feature are determined as follows:</span></span>

-   <span data-ttu-id="471c3-116">Если компонент не содержит компонентов, INSTALLSTATE \_ Local и InstallState \_ Source являются допустимыми состояниями для функции.</span><span class="sxs-lookup"><span data-stu-id="471c3-116">If the feature does not contain components, both INSTALLSTATE\_LOCAL and INSTALLSTATE\_SOURCE are valid states for the feature.</span></span>
-   <span data-ttu-id="471c3-117">Если хотя бы один компонент компонента имеет атрибут Мсидбкомпонентаттрибутеслокалонли или Мсидбкомпонентаттрибутесоптионал, INSTALLSTATE \_ local является допустимым состоянием для этой функции.</span><span class="sxs-lookup"><span data-stu-id="471c3-117">If at least one component of the feature has an attribute of msidbComponentAttributesLocalOnly or msidbComponentAttributesOptional, INSTALLSTATE\_LOCAL is a valid state for the feature.</span></span>
-   <span data-ttu-id="471c3-118">Если хотя бы один компонент компонента имеет атрибут Мсидбкомпонентаттрибутессаурцеонли или Мсидбкомпонентаттрибутесоптионал, INSTALLSTATE \_ source является допустимым состоянием для этой функции.</span><span class="sxs-lookup"><span data-stu-id="471c3-118">If at least one component of the feature has an attribute of msidbComponentAttributesSourceOnly or msidbComponentAttributesOptional, INSTALLSTATE\_SOURCE is a valid state for the feature.</span></span>
-   <span data-ttu-id="471c3-119">Если файл компонента, относящегося к компоненту, исправлен или находится в сжатом источнике, INSTALLSTATE \_ source не включается в качестве допустимого состояния для этой функции.</span><span class="sxs-lookup"><span data-stu-id="471c3-119">If a file of a component belonging to the feature is patched or from a compressed source, then INSTALLSTATE\_SOURCE is not included as a valid state for the feature.</span></span>
-   <span data-ttu-id="471c3-120">\_Объявление InstallState не является допустимым, если компонент запретил объявление (мсидбфеатуреаттрибутесдисалловадвертисе) или компонент требует поддержки платформы для объявления (мсидбфеатуреаттрибутеснаунсуппортедадвертисе), а платформа не поддерживает ее.</span><span class="sxs-lookup"><span data-stu-id="471c3-120">INSTALLSTATE\_ADVERTISE is not a valid state if the feature disallows advertisement (msidbFeatureAttributesDisallowAdvertise) or the feature requires platform support for advertisement (msidbFeatureAttributesNoUnsupportedAdvertise) and the platform does not support it.</span></span>
-   <span data-ttu-id="471c3-121">INSTALLSTATE \_ отсутствует — допустимое состояние для функции, если его атрибуты не включают мсидбфеатуреаттрибутесуидисалловабсент.</span><span class="sxs-lookup"><span data-stu-id="471c3-121">INSTALLSTATE\_ABSENT is a valid state for the feature if its attributes do not include msidbFeatureAttributesUIDisallowAbsent.</span></span>
-   <span data-ttu-id="471c3-122">Допустимые состояния дочерних компонентов, помеченных для выполнения родительского компонента (Мсидбфеатуреаттрибутесфолловпарент), основаны на действии родительского компонента или установленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="471c3-122">Valid states for child features marked to follow the parent feature (msidbFeatureAttributesFollowParent) are based upon the parent feature's action or installed state.</span></span>

<span data-ttu-id="471c3-123">Если свойство завершается неудачно, можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="471c3-123">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="471c3-124">Требования</span><span class="sxs-lookup"><span data-stu-id="471c3-124">Requirements</span></span>



| <span data-ttu-id="471c3-125">Требование</span><span class="sxs-lookup"><span data-stu-id="471c3-125">Requirement</span></span> | <span data-ttu-id="471c3-126">Значение</span><span class="sxs-lookup"><span data-stu-id="471c3-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="471c3-127">Версия</span><span class="sxs-lookup"><span data-stu-id="471c3-127">Version</span></span><br/> | <span data-ttu-id="471c3-128">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="471c3-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="471c3-129">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="471c3-129">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="471c3-130">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="471c3-130">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="471c3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="471c3-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="471c3-132"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="471c3-132"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="471c3-133">IID</span><span class="sxs-lookup"><span data-stu-id="471c3-133">IID</span></span><br/>     | <span data-ttu-id="471c3-134">IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="471c3-134">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




