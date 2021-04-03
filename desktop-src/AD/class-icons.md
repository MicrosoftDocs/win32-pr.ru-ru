---
title: Значки классов
description: Значок, используемый для представления объекта класса, можно указать в атрибуте iconPath контейнера ДисплайспеЦифиерс.
ms.assetid: 0ff8da8a-d3d3-4a15-8103-4fe6ec307427
ms.tgt_platform: multiple
keywords:
- Отображение имен классов AD, значки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691d4ef22babeded12ec9b951f92247df99521b6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103987352"
---
# <a name="class-icons"></a><span data-ttu-id="d04b2-104">Значки классов</span><span class="sxs-lookup"><span data-stu-id="d04b2-104">Class Icons</span></span>

<span data-ttu-id="d04b2-105">Значок, используемый для представления объекта класса, можно указать в атрибуте **iconPath** контейнера дисплайспеЦифиерс.</span><span class="sxs-lookup"><span data-stu-id="d04b2-105">The icon used to represent a class object can be specified in the **iconPath** attribute in the DisplaySpecifiers container.</span></span> <span data-ttu-id="d04b2-106">Более того, каждый класс может хранить несколько состояний значков.</span><span class="sxs-lookup"><span data-stu-id="d04b2-106">Moreover, each class can store multiple icon states.</span></span> <span data-ttu-id="d04b2-107">Например, класс папки может иметь значки для открытых, закрытых и отключенных состояний.</span><span class="sxs-lookup"><span data-stu-id="d04b2-107">For example, a folder class can have icons for the open, closed, and disabled states.</span></span> <span data-ttu-id="d04b2-108">Текущая реализация принимает максимум шестнадцати различных состояний значков для каждого класса.</span><span class="sxs-lookup"><span data-stu-id="d04b2-108">The current implementation accepts a maximum of sixteen different icon states per class.</span></span>

<span data-ttu-id="d04b2-109">Атрибут **iconPath** можно указать одним из двух способов.</span><span class="sxs-lookup"><span data-stu-id="d04b2-109">The **iconPath** attribute can be specified in one of two ways.</span></span>


```C++
<state>,<icon file name>
```



<span data-ttu-id="d04b2-110">или</span><span class="sxs-lookup"><span data-stu-id="d04b2-110">or</span></span>


```C++
<state>,<module file name>,<resource ID>
```



<span data-ttu-id="d04b2-111">В этих примерах " &lt; State &gt; " — это целое число со значением от 0 до 15.</span><span class="sxs-lookup"><span data-stu-id="d04b2-111">In these examples, the "&lt;state&gt;" is an integer with a value between 0 and 15.</span></span> <span data-ttu-id="d04b2-112">Значение 0 определяется по умолчанию или закрытому состоянию значка.</span><span class="sxs-lookup"><span data-stu-id="d04b2-112">The value 0 is defined to be the default or closed state of the icon.</span></span> <span data-ttu-id="d04b2-113">Значение 1 определяется как открытое состояние значка.</span><span class="sxs-lookup"><span data-stu-id="d04b2-113">The value 1 is defined to be the open state of the icon.</span></span> <span data-ttu-id="d04b2-114">Значение 2 — отключенное состояние.</span><span class="sxs-lookup"><span data-stu-id="d04b2-114">The value 2 is the disabled state.</span></span> <span data-ttu-id="d04b2-115">Все остальные значения определяются приложением.</span><span class="sxs-lookup"><span data-stu-id="d04b2-115">All other values are application-defined.</span></span>

<span data-ttu-id="d04b2-116">" &lt; Имя файла значка &gt; " — это путь и имя файла значка, содержащего изображение значка.</span><span class="sxs-lookup"><span data-stu-id="d04b2-116">The "&lt;icon file name&gt;" is the path and file name of an icon file that contains the icon image.</span></span>

<span data-ttu-id="d04b2-117">" &lt; Имя файла модуля &gt; " — это путь и имя файла модуля, например EXE или DLL, который содержит изображение значка в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="d04b2-117">The "&lt;module file name&gt;" is the path and file name of a module, such as an EXE or DLL, that contains the icon image in a resource.</span></span> <span data-ttu-id="d04b2-118">" &lt; Идентификатор ресурса &gt; " — это целое число, которое указывает идентификатор ресурса значка в модуле.</span><span class="sxs-lookup"><span data-stu-id="d04b2-118">The "&lt;resource ID&gt;" is an integer that specifies the resource identifier of the icon resource within the module.</span></span>

## <a name="adding-a-value-to-the-iconpath-attribute"></a><span data-ttu-id="d04b2-119">Добавление значения к атрибуту **iconPath**</span><span class="sxs-lookup"><span data-stu-id="d04b2-119">Adding a Value to the **iconPath** Attribute</span></span>

<span data-ttu-id="d04b2-120">Чтобы добавить значение в атрибут **iconPath** , выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d04b2-120">To add a value to the **iconPath** attribute, perform the following steps.</span></span>

1.  <span data-ttu-id="d04b2-121">Определить, существует ли значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="d04b2-121">Determine if the value for the attribute exists.</span></span> <span data-ttu-id="d04b2-122">Если значение должно быть заменено, сначала удалите существующее значение с помощью метода [**iAds::P утекс**](/windows/desktop/api/iads/nf-iads-iads-putex) с параметром *лнконтролкоде* , для которого установлено **свойство ADS \_ \_** , а для параметра *впроп* — значение, которое необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="d04b2-122">If a value is to be replaced, first, delete the existing value using the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method with the *lnControlCode* parameter set to **ADS\_PROPERTY\_DELETE** and the *vProp* parameter set to the value to be removed.</span></span> <span data-ttu-id="d04b2-123">Не используйте свойство **ADS \_ \_ Очистка** или **\_ \_ Обновление свойства ADS** для *лнконтролкоде*.</span><span class="sxs-lookup"><span data-stu-id="d04b2-123">Do not use **ADS\_PROPERTY\_CLEAR** or **ADS\_PROPERTY\_UPDATE** for *lnControlCode*.</span></span>
2.  <span data-ttu-id="d04b2-124">Создайте строку, представляющую данные значка атрибута.</span><span class="sxs-lookup"><span data-stu-id="d04b2-124">Create the string that represents the attribute icon data.</span></span> <span data-ttu-id="d04b2-125">Пример см. в приведенном выше формате.</span><span class="sxs-lookup"><span data-stu-id="d04b2-125">For an example, see the format above.</span></span>
3.  <span data-ttu-id="d04b2-126">Чтобы добавить новое значение, используйте метод [**iAds::P утекс**](/windows/desktop/api/iads/nf-iads-iads-putex) с параметром *лнконтролкоде* , для которого установлено **значение \_ AD \_ append**.</span><span class="sxs-lookup"><span data-stu-id="d04b2-126">To add the new value, use the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method with the *lnControlCode* parameter set to **ADS\_PROPERTY\_APPEND**.</span></span>
4.  <span data-ttu-id="d04b2-127">Чтобы зафиксировать изменения в каталоге, вызовите функцию [**iAds:: сетинфо**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span><span class="sxs-lookup"><span data-stu-id="d04b2-127">To commit changes to the directory, call [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span></span>

 

 