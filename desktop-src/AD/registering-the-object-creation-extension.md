---
title: Регистрация расширения создания объекта
description: При создании библиотеки DLL расширения создания объектов в домен Active Directory Services она должна быть зарегистрирована в реестре Windows и службах домен Active Directory для создания COM и оснасток Active Directory администрирования консоли MMC, осведомленных о расширении.
ms.assetid: 6e950c6c-1a4f-4de0-9be1-004c31d4734c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27d8e2a50c2340d678fd43e546d68525afbc8a7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103987314"
---
# <a name="registering-the-object-creation-extension"></a><span data-ttu-id="bac48-103">Регистрация расширения создания объекта</span><span class="sxs-lookup"><span data-stu-id="bac48-103">Registering the Object Creation Extension</span></span>

<span data-ttu-id="bac48-104">При создании библиотеки DLL расширения создания объектов в домен Active Directory Services она должна быть зарегистрирована в реестре Windows и службах домен Active Directory для создания COM и оснасток Active Directory администрирования консоли MMC, осведомленных о расширении.</span><span class="sxs-lookup"><span data-stu-id="bac48-104">When an object creation extension DLL in Active Directory Domain Services is created, it must be registered with the Windows registry and Active Directory Domain Services to make COM and the Active Directory administrative MMC snap-ins aware of the extension.</span></span>

## <a name="registering-in-the-windows-registry"></a><span data-ttu-id="bac48-105">Регистрация в реестре Windows</span><span class="sxs-lookup"><span data-stu-id="bac48-105">Registering in the Windows Registry</span></span>

<span data-ttu-id="bac48-106">Как и все серверы COM, расширение создания объектов должно быть зарегистрировано в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="bac48-106">Like all COM servers, an object creation extension must be registered in the Windows registry.</span></span> <span data-ttu-id="bac48-107">Расширение регистрируется в следующем разделе:</span><span class="sxs-lookup"><span data-stu-id="bac48-107">The extension is registered under the following key:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      <extension CLSID>
         InProcServer32
            (Default) = <extension path>
            ThreadingModel = Apartment
```

<span data-ttu-id="bac48-108">" &lt; Extension CLSID &gt; " — это строковое представление идентификатора CLSID, созданное функцией [**стрингфромклсид**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="bac48-108">"&lt;extension CLSID&gt;" is the string representation of the CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span> <span data-ttu-id="bac48-109">" &lt; путь расширения &gt; " содержит путь и имя файла DLL расширения.</span><span class="sxs-lookup"><span data-stu-id="bac48-109">"&lt;extension path&gt;" contains the path and file name of the extension DLL.</span></span> <span data-ttu-id="bac48-110">Значение **ThreadingModel** для всех расширений создания объектов должно быть "апартаментом".</span><span class="sxs-lookup"><span data-stu-id="bac48-110">The **ThreadingModel** value for all object creation extensions must be "Apartment".</span></span>

## <a name="registering-with-active-directory-domain-services"></a><span data-ttu-id="bac48-111">Регистрация в домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="bac48-111">Registering with Active Directory Domain Services</span></span>

<span data-ttu-id="bac48-112">Регистрация расширения для создания объектов относится только к одному языку.</span><span class="sxs-lookup"><span data-stu-id="bac48-112">Object creation extension registration is specific to one locale.</span></span> <span data-ttu-id="bac48-113">Если расширение создания объектов применяется ко всем языкам, оно должно быть зарегистрировано в объекте **дисплайспеЦифиер** класса Object во всех подконтейнерах языкового стандарта контейнера дисплайспеЦифиерс.</span><span class="sxs-lookup"><span data-stu-id="bac48-113">If the object creation extension applies to all locales, it must be registered in the object class's **displaySpecifier** object in all of the locale subcontainers in the DisplaySpecifiers container.</span></span> <span data-ttu-id="bac48-114">Если расширение создания объекта локализовано для определенного языкового стандарта, зарегистрируйте его в объекте **дисплайспеЦифиер** в подконтейнере этого языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="bac48-114">If the object creation extension is localized for a certain locale, register it in the **displaySpecifier** object in that locale's subcontainer.</span></span> <span data-ttu-id="bac48-115">Дополнительные сведения о контейнере ДисплайспеЦифиерс и языковых стандартах см. в разделе [описатели экрана](display-specifiers.md) и [контейнеры дисплайспеЦифиерс](displayspecifiers-container.md).</span><span class="sxs-lookup"><span data-stu-id="bac48-115">For more information about the DisplaySpecifiers container and locales, see [Display Specifiers](display-specifiers.md) and [DisplaySpecifiers Container](displayspecifiers-container.md).</span></span>

<span data-ttu-id="bac48-116">Существует два атрибута ДисплайспеЦифиер, в которых можно зарегистрировать расширение создания объектов.</span><span class="sxs-lookup"><span data-stu-id="bac48-116">There are two DisplaySpecifier attributes that an object creation extension can be registered under.</span></span> <span data-ttu-id="bac48-117">Это **креатионвизард** и **креатевизардекст**.</span><span class="sxs-lookup"><span data-stu-id="bac48-117">These are **creationWizard** and **createWizardExt**.</span></span>

<span data-ttu-id="bac48-118">Атрибут **креатионвизард** определяет расширения создания первичных объектов для замены существующего или собственного мастера создания объектов в Active Directory административных оснастках. Первичное расширение создания предоставляет первый набор страниц и размещается так же, как и собственные страницы.</span><span class="sxs-lookup"><span data-stu-id="bac48-118">The **creationWizard** attribute identifies primary object creation extensions to replace the existing or native object creation wizard in Active Directory administrative snap-ins. A primary creation extension provides the first set of pages and is hosted in the same way as native pages.</span></span> <span data-ttu-id="bac48-119">Этот атрибут является однозначным и требует следующего формата:</span><span class="sxs-lookup"><span data-stu-id="bac48-119">This attribute is single-valued and requires the following format:</span></span>


```C++
<CLSID>
```



<span data-ttu-id="bac48-120">" &lt; CLSID &gt; " — это строковое представление CLSID COM-объекта, созданное функцией [**стрингфромклсид**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="bac48-120">The "&lt;CLSID&gt;" is the string representation of the COM object's CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span>

<span data-ttu-id="bac48-121">Атрибут **креатевизардекст** определяет расширения для создания дополнительного объекта.</span><span class="sxs-lookup"><span data-stu-id="bac48-121">The **createWizardExt** attribute identifies secondary object creation extensions.</span></span> <span data-ttu-id="bac48-122">Вторичное расширение создания добавляет страницы мастера к собственным страницам или первичному расширению.</span><span class="sxs-lookup"><span data-stu-id="bac48-122">A secondary creation extension adds wizard pages to the native pages or primary extension.</span></span> <span data-ttu-id="bac48-123">Этот атрибут имеет несколько значений и требует следующего формата:</span><span class="sxs-lookup"><span data-stu-id="bac48-123">This attribute is multi-valued and requires the following format:</span></span>


```C++
<order number>,<CLSID>
```



<span data-ttu-id="bac48-124">&lt;Порядковый номер &gt; — это число без знака, представляющее расположение страницы в мастере.</span><span class="sxs-lookup"><span data-stu-id="bac48-124">The "&lt;order number&gt;" is an unsigned number that represents the page's position in the wizard.</span></span> <span data-ttu-id="bac48-125">При отображении мастера создания значения сортируются с помощью сравнения "номер заказа" каждого значения &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="bac48-125">When a creation wizard is displayed, the values are sorted using a comparison of each value's "&lt;order number&gt;".</span></span> <span data-ttu-id="bac48-126">Если несколько значений имеют одинаковый &lt; порядковый номер &gt; , эти страницы загружаются в том порядке, в котором они считываются с Active Directory сервера.</span><span class="sxs-lookup"><span data-stu-id="bac48-126">If more than one value has the same "&lt;order number&gt;", those pages are loaded in the order they are read from the Active Directory server.</span></span> <span data-ttu-id="bac48-127">По возможности следует использовать несуществующий " &lt; номер заказа &gt; " (то есть тот, который не использовался другими значениями в свойстве).</span><span class="sxs-lookup"><span data-stu-id="bac48-127">If possible, you should use a non-existing "&lt;order number&gt;" (that is, one that has not been used by other values in the property).</span></span> <span data-ttu-id="bac48-128">Нет предписанной начальной должности, и в &lt; последовательности "номер заказа" могут пропуски &gt; .</span><span class="sxs-lookup"><span data-stu-id="bac48-128">There is no prescribed starting position, and gaps are allowed in the "&lt;order number&gt;" sequence.</span></span>

<span data-ttu-id="bac48-129">" &lt; CLSID &gt; " — это строковое представление CLSID COM-объекта, созданное функцией [**стрингфромклсид**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="bac48-129">The "&lt;CLSID&gt;" is the string representation of the COM object's CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span>

 

 