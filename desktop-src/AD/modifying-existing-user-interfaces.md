---
title: Изменение существующих пользовательских интерфейсов
description: На панели результатов оснастки MMC "Active Directory пользователи и компьютеры" отображается несколько столбцов данных атрибутов для объектов в контейнере, таких как атрибуты Name и Description.
ms.assetid: 55f4ae82-c380-42a9-beba-047ffd0131eb
ms.tgt_platform: multiple
keywords:
- Изменение существующих пользовательских интерфейсов AD
- Оснастка "пользователи и компьютеры" (AD), изменение экрана
- Оснастка "пользователи и компьютеры" (AD), Добавление столбцов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0765988a9ceed3e98966091ad94b868b96fd88
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887643"
---
# <a name="modifying-existing-user-interfaces"></a><span data-ttu-id="e95d4-106">Изменение существующих пользовательских интерфейсов</span><span class="sxs-lookup"><span data-stu-id="e95d4-106">Modifying Existing User Interfaces</span></span>

<span data-ttu-id="e95d4-107">На панели результатов оснастки MMC "Active Directory пользователи и компьютеры" отображается несколько столбцов данных атрибутов для объектов в контейнере, таких как атрибуты **Name** и **Description** .</span><span class="sxs-lookup"><span data-stu-id="e95d4-107">The results pane of the Active Directory Users and Computers MMC snap-in displays several columns of attribute data for objects within a container, such as the **Name** and **Description** attributes.</span></span> <span data-ttu-id="e95d4-108">Оснастка позволяет пользователю добавлять и удалять столбцы, отображаемые на панели результатов оснастки.</span><span class="sxs-lookup"><span data-stu-id="e95d4-108">The snap-in enables the user to add and remove the columns displayed in the results pane of the snap-in.</span></span>

<span data-ttu-id="e95d4-109">Чтобы изменить отображение, пользователь использует раскрывающееся меню **вид** и выбирает пункт **Добавить или удалить столбцы**.</span><span class="sxs-lookup"><span data-stu-id="e95d4-109">To change the display, the user uses the **View** pull-down menu and selects **Add/Remove Columns**.</span></span> <span data-ttu-id="e95d4-110">В диалоговом окне **Добавление или удаление столбцов** имеется список столбцов, которые пользователь может выбрать для вывода в области результатов.</span><span class="sxs-lookup"><span data-stu-id="e95d4-110">In the **Add/Remove Columns** dialog box, there is a list of columns that the user can choose from to display in the results pane.</span></span>

<span data-ttu-id="e95d4-111">Оснастка MMC Active Directory пользователи и компьютеры, входящая в состав Windows Server 2003, Standard Edition, Windows Server 2003, Enterprise Edition и Windows Server 2003, Datacenter Edition, предоставляет возможность изменять список столбцов, которые могут отображаться на панели результатов оснастки для контейнера.</span><span class="sxs-lookup"><span data-stu-id="e95d4-111">The Active Directory Users and Computers MMC snap-in that is included with Windows Server 2003, Standard Edition, Windows Server 2003, Enterprise Edition, and Windows Server 2003, Datacenter Edition, provides the ability to modify the list of columns that can be displayed in the results pane of the snap-in for a container.</span></span> <span data-ttu-id="e95d4-112">Эта функция существует только в том случае, если оснастка нацелена на лес со схемой Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e95d4-112">This feature only exists if the snap-in is targeted at a forest with Windows Server 2003 schema.</span></span>

<span data-ttu-id="e95d4-113">Чтобы добавить столбец в список, добавьте значение в атрибут **екстраколумнс** описателя вывода для типа объекта, с которым связан атрибут.</span><span class="sxs-lookup"><span data-stu-id="e95d4-113">To add a column to the list, add a value to the **extraColumns** attribute of the display specifier for the object type that the attribute is associated with.</span></span> <span data-ttu-id="e95d4-114">Атрибут **екстраколумнс** представляет собой строковый атрибут с несколькими значениями, в котором каждая строка имеет следующий формат.</span><span class="sxs-lookup"><span data-stu-id="e95d4-114">The **extraColumns** attribute is a multi-valued string attribute where each string is in the following format.</span></span>


```C++

<ldapdisplayname>,<column header>,<default visibility>,<width>,<unused>

```



<span data-ttu-id="e95d4-115">В следующей таблице приведено содержимое этих значений.</span><span class="sxs-lookup"><span data-stu-id="e95d4-115">The following table lists the contents of these values.</span></span>



| <span data-ttu-id="e95d4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e95d4-116">Value</span></span>                        | <span data-ttu-id="e95d4-117">Описание</span><span class="sxs-lookup"><span data-stu-id="e95d4-117">Description</span></span>                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e95d4-118">" &lt; LdapDisplayName &gt; "</span><span class="sxs-lookup"><span data-stu-id="e95d4-118">"&lt;ldapdisplayname&gt;"</span></span>    | <span data-ttu-id="e95d4-119">Содержит строку, представляющую атрибут **LdapDisplayName** атрибута.</span><span class="sxs-lookup"><span data-stu-id="e95d4-119">Contains a string that represents the **ldapDisplayName** of the attribute.</span></span>                                                         |
| <span data-ttu-id="e95d4-120">" &lt; заголовок столбца &gt; "</span><span class="sxs-lookup"><span data-stu-id="e95d4-120">"&lt;column header&gt;"</span></span>      | <span data-ttu-id="e95d4-121">Содержит строку, представляющую текст, отображаемый в заголовке столбца.</span><span class="sxs-lookup"><span data-stu-id="e95d4-121">Contains a string that represents the text displayed in the header for the column.</span></span>                                                  |
| <span data-ttu-id="e95d4-122">" &lt; видимость по умолчанию &gt; "</span><span class="sxs-lookup"><span data-stu-id="e95d4-122">"&lt;default visibility&gt;"</span></span> | <span data-ttu-id="e95d4-123">Содержит числовое значение, равное 0, если атрибут скрыт по умолчанию, или 1, если атрибут видим по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e95d4-123">Contains a numeric value that is 0 if the attribute is hidden by default or 1 if the attribute is visible by default.</span></span>               |
| <span data-ttu-id="e95d4-124">" &lt; Width &gt; "</span><span class="sxs-lookup"><span data-stu-id="e95d4-124">"&lt;width&gt;"</span></span>              | <span data-ttu-id="e95d4-125">Содержит ширину столбца в пикселях.</span><span class="sxs-lookup"><span data-stu-id="e95d4-125">Contains the width of the column, in pixels.</span></span> <span data-ttu-id="e95d4-126">Если это значение равно-1, ширина столбца устанавливается равным ширине заголовка столбца.</span><span class="sxs-lookup"><span data-stu-id="e95d4-126">If this value is -1, the width of the column is set to the width of the column header.</span></span> |
| <span data-ttu-id="e95d4-127">"не &lt; используется &gt; "</span><span class="sxs-lookup"><span data-stu-id="e95d4-127">"&lt;unused&gt;"</span></span>             | <span data-ttu-id="e95d4-128">Не используется.</span><span class="sxs-lookup"><span data-stu-id="e95d4-128">Unused.</span></span> <span data-ttu-id="e95d4-129">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e95d4-129">Must be zero.</span></span>                                                                                                               |



 

<span data-ttu-id="e95d4-130">Например, чтобы добавить столбец, который будет отображать каноническое имя для объектов в подразделении, значение атрибута **каноникалнаме** добавляется в атрибут **екстраколумнс** объекта **OrganizationalUnit-дисплея** в контейнере описатели вывода.</span><span class="sxs-lookup"><span data-stu-id="e95d4-130">For example, to add a column that will display the canonical name for objects in an organizational unit, a value for the **canonicalName** attribute is added to the **extraColumns** attribute of the **organizationalUnit-Display** object in the display specifiers container.</span></span> <span data-ttu-id="e95d4-131">Строка, добавляемая в атрибут **екстраколумнс** объекта **OrganizationalUnit-дисплея** , будет выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="e95d4-131">The string added to the **extraColumns** attribute of the **organizationalUnit-Display** object will look like the following.</span></span>


```C++
canonicalName,Canonical Name,0,150,0
```



<span data-ttu-id="e95d4-132">В диалоговом окне **Добавление или удаление столбцов** отображаются только столбцы, содержащиеся в атрибуте **екстраколумнс** объекта **дисплайспеЦифиер** типа контейнера, который отображается.</span><span class="sxs-lookup"><span data-stu-id="e95d4-132">The **Add/Remove Columns** dialog box displays only the columns that are contained in the **extraColumns** attribute of the **displaySpecifier** object of the container type that is being displayed.</span></span> <span data-ttu-id="e95d4-133">Если атрибут **екстраколумнс** не содержит значений, в диалоговом окне **Добавление или удаление столбцов** будет отображен фиксированный набор столбцов.</span><span class="sxs-lookup"><span data-stu-id="e95d4-133">If the **extraColumns** attribute does not contain any values, the **Add/Remove Columns** dialog box will display a fixed set of columns.</span></span> <span data-ttu-id="e95d4-134">Копия фиксированного набора столбцов содержится в атрибуте **екстраколумнс** объекта, **отображаемого по умолчанию** .</span><span class="sxs-lookup"><span data-stu-id="e95d4-134">A copy of the fixed set of columns is contained in the **extraColumns** attribute of the **default-Display** object.</span></span>

<span data-ttu-id="e95d4-135">Чтобы добавить один или несколько столбцов в список столбцов для определенного объекта, необходимо скопировать все значения **екстраколумнс** из объекта, **отображаемого по умолчанию** , в целевой объект, а затем добавить пользовательские столбцы.</span><span class="sxs-lookup"><span data-stu-id="e95d4-135">To add one or more columns to the list of columns for a specific object, you must copy all of the **extraColumns** values from the **default-Display** object to the target object and then add the custom columns.</span></span> <span data-ttu-id="e95d4-136">Если указать атрибут **екстраколумнс** для данного класса, то этот класс будет использовать эти столбцы и не будет объединять их со столбцами, указанными в классе, **используемом по умолчанию** .</span><span class="sxs-lookup"><span data-stu-id="e95d4-136">If you specify the **extraColumns** attribute on a given class, then that class will use those columns and will not merge them with the columns that are specified in the **default-Display** class.</span></span> <span data-ttu-id="e95d4-137">Поэтому дальнейшие изменения в классе, **используемом по умолчанию** , не будут влиять на этот объект.</span><span class="sxs-lookup"><span data-stu-id="e95d4-137">Therefore, further changes to the **default-Display** class will have no effect on that object.</span></span>

<span data-ttu-id="e95d4-138">Чтобы отобразить пользовательский столбец для всех типов контейнеров, для которых не зарегистрированы настраиваемые столбцы, добавьте значение для столбца в атрибут **екстраколумнс** объекта, **отображаемого по умолчанию** .</span><span class="sxs-lookup"><span data-stu-id="e95d4-138">To display a custom column for all container types that do not have any custom columns registered, add a value for the column to the **extraColumns** attribute of the **default-Display** object.</span></span>

 

 




