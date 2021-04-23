---
description: Свойство Феатуререкуестстате — это свойство для чтения и записи объекта Session.
ms.assetid: ba19603b-ac81-4a8b-81ca-ad5f28974599
title: Свойство Session. Феатуререкуестстате
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1531157ab094d817d34650f8eae2ac6dc23c681c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675428"
---
# <a name="sessionfeaturerequeststate-property"></a><span data-ttu-id="25610-103">Свойство Session. Феатуререкуестстате</span><span class="sxs-lookup"><span data-stu-id="25610-103">Session.FeatureRequestState property</span></span>

<span data-ttu-id="25610-104">Свойство **феатуререкуестстате** — это свойство для чтения и записи объекта [**Session**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="25610-104">The **FeatureRequestState** property is a read-write property of the [**Session**](session-object.md) object.</span></span> <span data-ttu-id="25610-105">Его можно использовать для получения текущего состояния действия функции или запроса изменений в действии функции и ее подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="25610-105">It can be used to obtain the current action state of a feature or to request a change in the action of a feature and its subfeatures.</span></span> <span data-ttu-id="25610-106">Эта функция должна называться в таблице [Feature](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="25610-106">The feature must be named in the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="25610-107">Если запрашивается изменение состояния действия компонента, также может быть изменено состояние действия всех компонентов измененного компонента.</span><span class="sxs-lookup"><span data-stu-id="25610-107">If a change to the action state of a feature is requested, the action state of all components of the changed feature may be changed as well.</span></span> <span data-ttu-id="25610-108">Состояние действия компонентов, совместно используемых несколькими компонентами, будет изменено в соответствии с новым состоянием действия функции (см. примечания).</span><span class="sxs-lookup"><span data-stu-id="25610-108">The action state of components shared by more than one feature will be changed as appropriate based on the new feature action state (see Remarks).</span></span> <span data-ttu-id="25610-109">Свойство **феатуререкуестстате** можно также использовать для настройки всех компонентов одновременно, указав ключевое слово ALL вместо имени конкретного компонента.</span><span class="sxs-lookup"><span data-stu-id="25610-109">The **FeatureRequestState** property can also be used to configure all features at once by specifying the keyword ALL instead of a specific feature name.</span></span>

<span data-ttu-id="25610-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="25610-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="25610-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25610-111">Syntax</span></span>


```JScript
propVal = Session.FeatureRequestState
Session.FeatureRequestState = propVal 
```



## <a name="property-value"></a><span data-ttu-id="25610-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="25610-112">Property value</span></span>

<span data-ttu-id="25610-113">Обязательная строка, указывающая имя настраиваемого компонента.</span><span class="sxs-lookup"><span data-stu-id="25610-113">Required string that specifies the name of the feature to be configured.</span></span> <span data-ttu-id="25610-114">Чтобы задать для всех компонентов требуемое состояние запроса, используйте зарезервированное слово без учета регистра: ALL.</span><span class="sxs-lookup"><span data-stu-id="25610-114">To set all features to a desired request state, use the reserved case-insensitive word: ALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="25610-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="25610-115">Remarks</span></span>

<span data-ttu-id="25610-116">Перед вызовом **феатуререкуестстате** необходимо вызвать метод [**сетинсталллевел**](session-setinstalllevel.md) .</span><span class="sxs-lookup"><span data-stu-id="25610-116">The [**SetInstallLevel**](session-setinstalllevel.md) method must be called before calling **FeatureRequestState**.</span></span>

<span data-ttu-id="25610-117">Если текущее состояние компонента запрашивается, свойство **феатуререкуестстате** возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="25610-117">If the current state of the feature is being requested, the **FeatureRequestState** property returns one of the following values.</span></span>



| <span data-ttu-id="25610-118">Имя состояния выбора</span><span class="sxs-lookup"><span data-stu-id="25610-118">Selection state name</span></span>         | <span data-ttu-id="25610-119">Значение</span><span class="sxs-lookup"><span data-stu-id="25610-119">Meaning</span></span>                                                               |
|------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="25610-120">Мсиинсталлстатеункновн =-1</span><span class="sxs-lookup"><span data-stu-id="25610-120">msiInstallStateUnknown = -1</span></span>  | <span data-ttu-id="25610-121">Для функции не предпринимается никаких действий.</span><span class="sxs-lookup"><span data-stu-id="25610-121">No action is taken for the feature.</span></span> <span data-ttu-id="25610-122">Это эквивалентно значению NULL.</span><span class="sxs-lookup"><span data-stu-id="25610-122">This is equivalent to null.</span></span>       |
| <span data-ttu-id="25610-123">Мсиинсталлстатеадвертисед = 1</span><span class="sxs-lookup"><span data-stu-id="25610-123">msiInstallStateAdvertised =1</span></span> | <span data-ttu-id="25610-124">Функция должна быть объявлена.</span><span class="sxs-lookup"><span data-stu-id="25610-124">Feature is to be advertised.</span></span>                                          |
| <span data-ttu-id="25610-125">Мсиинсталлстатеабсент = 2</span><span class="sxs-lookup"><span data-stu-id="25610-125">msiInstallStateAbsent = 2</span></span>    | <span data-ttu-id="25610-126">Компонент будет удален.</span><span class="sxs-lookup"><span data-stu-id="25610-126">Feature is to be removed.</span></span>                                             |
| <span data-ttu-id="25610-127">Мсиинсталлстателокал = 3</span><span class="sxs-lookup"><span data-stu-id="25610-127">msiInstallStateLocal = 3</span></span>     | <span data-ttu-id="25610-128">Компонент должен быть установлен в качестве локальной для запуска.</span><span class="sxs-lookup"><span data-stu-id="25610-128">Feature is to be installed as run-local.</span></span>                              |
| <span data-ttu-id="25610-129">Мсиинсталлстатесаурце = 4</span><span class="sxs-lookup"><span data-stu-id="25610-129">msiInstallStateSource = 4</span></span>    | <span data-ttu-id="25610-130">Компонент должен быть установлен в качестве запуска с исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="25610-130">Feature is to be installed as run-from-source.</span></span>                        |
| <span data-ttu-id="25610-131">Мсиинсталлстатедефаулт = 5</span><span class="sxs-lookup"><span data-stu-id="25610-131">msiInstallStateDefault = 5</span></span>   | <span data-ttu-id="25610-132">Компонент должен быть переустановлен с текущим состоянием действия функции.</span><span class="sxs-lookup"><span data-stu-id="25610-132">Feature is to be reinstalled with the feature's current action state.</span></span> |



 

<span data-ttu-id="25610-133">Например, следующий пример получает текущее состояние "Мифеатуре" из настраиваемого действия VBScript.</span><span class="sxs-lookup"><span data-stu-id="25610-133">For example, the following obtains the current state of "MyFeature" from a VBScript custom action.</span></span>


```VB
Dim iRequestState
iRequestState = Session.FeatureRequestState("MyFeature")
```



<span data-ttu-id="25610-134">Если настраивается состояние компонента, свойству **феатуререкуестстате** должно быть присвоено одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="25610-134">If the state of the feature is being configured, the **FeatureRequestState** property should be set to one of the following values.</span></span>



| <span data-ttu-id="25610-135">Имя состояния выбора</span><span class="sxs-lookup"><span data-stu-id="25610-135">Selection state name</span></span>          | <span data-ttu-id="25610-136">Значение</span><span class="sxs-lookup"><span data-stu-id="25610-136">Meaning</span></span>                                 |
|-------------------------------|-----------------------------------------|
| <span data-ttu-id="25610-137">Мсиинсталлстатеадвертисед = 1</span><span class="sxs-lookup"><span data-stu-id="25610-137">msiInstallStateAdvertised = 1</span></span> | <span data-ttu-id="25610-138">Объявите функцию.</span><span class="sxs-lookup"><span data-stu-id="25610-138">Advertise the feature.</span></span>                  |
| <span data-ttu-id="25610-139">Мсиинсталлстатеабсент = 2</span><span class="sxs-lookup"><span data-stu-id="25610-139">msiInstallStateAbsent = 2</span></span>     | <span data-ttu-id="25610-140">Удалите компонент.</span><span class="sxs-lookup"><span data-stu-id="25610-140">Remove the feature.</span></span>                     |
| <span data-ttu-id="25610-141">Мсиинсталлстателокал = 3</span><span class="sxs-lookup"><span data-stu-id="25610-141">msiInstallStateLocal = 3</span></span>      | <span data-ttu-id="25610-142">Установите компонент в качестве локального запуска.</span><span class="sxs-lookup"><span data-stu-id="25610-142">Install the feature as run-local.</span></span>       |
| <span data-ttu-id="25610-143">Мсиинсталлстатесаурце = 4</span><span class="sxs-lookup"><span data-stu-id="25610-143">msiInstallStateSource = 4</span></span>     | <span data-ttu-id="25610-144">Установите компонент в качестве запуска из источника.</span><span class="sxs-lookup"><span data-stu-id="25610-144">Install the feature as run-from-source.</span></span> |



 

<span data-ttu-id="25610-145">Например, следующие запросы из настраиваемого действия VBScript, которые должны быть установлены для локального запуска на компьютере.</span><span class="sxs-lookup"><span data-stu-id="25610-145">For example, the following requests from a VBScript custom action that "MyFeature" be installed to run locally on the computer.</span></span>


```VB
Session.FeatureRequestState("MyFeature")=3
```



<span data-ttu-id="25610-146">При вызове **феатуререкуестстате** установщик пытается установить состояние действия каждого компонента, привязанного к указанному компоненту, в указанное состояние, как можно лучше.</span><span class="sxs-lookup"><span data-stu-id="25610-146">When **FeatureRequestState** is called, the installer attempts to set the action state of each component tied to the specified feature to the specified state, as best as possible.</span></span> <span data-ttu-id="25610-147">Однако существуют распространенные ситуации, когда запрос не может быть полностью одобрен.</span><span class="sxs-lookup"><span data-stu-id="25610-147">However, there are common situations when the request cannot be fully honored.</span></span> <span data-ttu-id="25610-148">Например, если функция привязана к двум компонентам, компоненту A и компоненту б, через таблицу [феатурекомпонентс](featurecomponents-table.md) и компонент a имеет атрибут **мсидбкомпонентаттрибутеслокалонли** , а компонент b имеет атрибут **мсидбкомпонентаттрибутессаурцеонли** .</span><span class="sxs-lookup"><span data-stu-id="25610-148">For example, if a feature is tied to two components, Component A and Component B, through the [FeatureComponents](featurecomponents-table.md) table and Component A has the **msidbComponentAttributesLocalOnly** attribute and component B has the **msidbComponentAttributesSourceOnly** attribute.</span></span> <span data-ttu-id="25610-149">В этом случае, если **феатуререкуестстате** вызывается с запрошенным состоянием либо мсиинсталлстателокал, либо мсиинсталлстатесаурце, запрос не может быть учтен для обоих компонентов.</span><span class="sxs-lookup"><span data-stu-id="25610-149">In this case, if **FeatureRequestState** is called with a requested state of either msiInstallStateLocal or msiInstallStateSource, the request cannot be honored for both components.</span></span> <span data-ttu-id="25610-150">В этом случае оба компонента можно включить с компонентом A, для которого задано значение Мсиинсталлстателокал, а для компонента B — значение Мсиинсталлстатесаурце.</span><span class="sxs-lookup"><span data-stu-id="25610-150">In this case, both components can be turned on with Component A set to msiInstallStateLocal and Component B set to msiInstallStateSource.</span></span>

<span data-ttu-id="25610-151">Если несколько компонентов связаны с одним компонентом, Последнее состояние действия этого компонента определяется следующим образом: если хотя бы один вызов компонента для установки компонента выполняется локально, он устанавливается Мсиинсталлстателокал.</span><span class="sxs-lookup"><span data-stu-id="25610-151">If more than one feature is linked to a single component, the final action state of that component is determined as follows: If at least one feature calls for the component to be installed locally, it is installed msiInstallStateLocal.</span></span> <span data-ttu-id="25610-152">Если по крайней мере один из функций вызывает запуск компонента с исходного носителя, он устанавливается Мсиинсталлстатесаурце.</span><span class="sxs-lookup"><span data-stu-id="25610-152">If at least one feature calls for the component to be run from the source media, it is installed msiInstallStateSource.</span></span> <span data-ttu-id="25610-153">Если по крайней мере один вызов функции для удаления компонента, действие имеет состояние Мсиинсталлстатеабсент.</span><span class="sxs-lookup"><span data-stu-id="25610-153">If at least one feature calls for the removal of the component, the action state is msiInstallStateAbsent.</span></span> <span data-ttu-id="25610-154">Дополнительные сведения о выборе компонентов для установки см. в таблице [Feature](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="25610-154">For more information on how features are selected for installation, see the [Feature](feature-table.md) table.</span></span>

<span data-ttu-id="25610-155">Если свойство завершается неудачно, можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="25610-155">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="25610-156">Требования</span><span class="sxs-lookup"><span data-stu-id="25610-156">Requirements</span></span>



| <span data-ttu-id="25610-157">Требование</span><span class="sxs-lookup"><span data-stu-id="25610-157">Requirement</span></span> | <span data-ttu-id="25610-158">Значение</span><span class="sxs-lookup"><span data-stu-id="25610-158">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25610-159">Версия</span><span class="sxs-lookup"><span data-stu-id="25610-159">Version</span></span><br/> | <span data-ttu-id="25610-160">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="25610-160">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="25610-161">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="25610-161">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="25610-162">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="25610-162">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="25610-163">DLL</span><span class="sxs-lookup"><span data-stu-id="25610-163">DLL</span></span><br/>     | <dl> <span data-ttu-id="25610-164"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25610-164"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="25610-165">IID</span><span class="sxs-lookup"><span data-stu-id="25610-165">IID</span></span><br/>     | <span data-ttu-id="25610-166">IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="25610-166">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="25610-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25610-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25610-168">**Session**</span><span class="sxs-lookup"><span data-stu-id="25610-168">**Session**</span></span>](session-object.md)
</dt> <dt>

[<span data-ttu-id="25610-169">Компонент</span><span class="sxs-lookup"><span data-stu-id="25610-169">Feature</span></span>](feature-table.md)
</dt> </dl>

 

 




