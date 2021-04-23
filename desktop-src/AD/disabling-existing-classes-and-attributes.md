---
title: Отключение существующих классов и атрибутов
description: Добавления схемы являются постоянными.
ms.assetid: 13ffd2f5-cf1d-4cde-a3d5-74cb5a44b6fc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74863d0d3c72f383259cfe262f4b7aa6fa27774a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773250"
---
# <a name="disabling-existing-classes-and-attributes"></a><span data-ttu-id="193b2-103">Отключение существующих классов и атрибутов</span><span class="sxs-lookup"><span data-stu-id="193b2-103">Disabling Existing Classes and Attributes</span></span>

<span data-ttu-id="193b2-104">Добавления схемы являются постоянными.</span><span class="sxs-lookup"><span data-stu-id="193b2-104">Schema additions are permanent.</span></span> <span data-ttu-id="193b2-105">Нельзя удалять объекты **attributeSchema** и **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="193b2-105">You cannot delete **attributeSchema** and **classSchema** objects.</span></span> <span data-ttu-id="193b2-106">В распределенной системе трудно гарантировать отсутствие экземпляров данного класса или атрибута.</span><span class="sxs-lookup"><span data-stu-id="193b2-106">In a distributed system, it is difficult to guarantee that there are no instances of a given class or attribute.</span></span> <span data-ttu-id="193b2-107">Удаление определения класса или атрибута повреждает существующие экземпляры этого класса или атрибута.</span><span class="sxs-lookup"><span data-stu-id="193b2-107">Removing the definition of a class or attribute damages existing instances of that class or attribute.</span></span>

<span data-ttu-id="193b2-108">Можно отключить существующий класс или атрибут, пометив его как "уничтоженный".</span><span class="sxs-lookup"><span data-stu-id="193b2-108">You can disable an existing class or attribute by marking it as "defunct".</span></span> <span data-ttu-id="193b2-109">Это не влияет на существующие экземпляры класса или атрибута таким образом, что отмечено, но не позволяет создавать новые экземпляры.</span><span class="sxs-lookup"><span data-stu-id="193b2-109">This does not affect existing instances of the class or attribute so marked, but it prevents the creation of new instances.</span></span>

<span data-ttu-id="193b2-110">При отключении классов и атрибутов схемы применяются следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="193b2-110">The following restrictions apply when disabling schema classes and attributes:</span></span>

-   <span data-ttu-id="193b2-111">Нельзя отключить класс или атрибут категории 1.</span><span class="sxs-lookup"><span data-stu-id="193b2-111">You cannot disable a Category 1 class or attribute.</span></span>
-   <span data-ttu-id="193b2-112">Нельзя отключить атрибут, который является членом класса, который также не отключен.</span><span class="sxs-lookup"><span data-stu-id="193b2-112">You cannot disable an attribute that is a member of a class that is not also disabled.</span></span> <span data-ttu-id="193b2-113">Это связано с тем, что для класса (не отключен) может потребоваться атрибут, и отключение атрибута предотвращает создание новых экземпляров класса.</span><span class="sxs-lookup"><span data-stu-id="193b2-113">This is because an attribute might be required for the (not disabled) class, and disabling the attribute prevents new instances of the class from being created.</span></span>

<span data-ttu-id="193b2-114">Чтобы **отключить атрибут, задайте атрибуту** **attributeSchema** объекта его значение **true**.</span><span class="sxs-lookup"><span data-stu-id="193b2-114">To disable an attribute, set the **isDefunct** attribute of its **attributeSchema** object to **TRUE**.</span></span> <span data-ttu-id="193b2-115">При отключении атрибута нельзя создать новые экземпляры атрибута.</span><span class="sxs-lookup"><span data-stu-id="193b2-115">When an attribute is disabled, new instances of the attribute cannot be created.</span></span> <span data-ttu-id="193b2-116">Чтобы повторно включить атрибут, установите для атрибута **уничтожение** **значение false**.</span><span class="sxs-lookup"><span data-stu-id="193b2-116">To re-enable the attribute set the **isDefunct** attribute to **FALSE**.</span></span>

<span data-ttu-id="193b2-117">Чтобы отключить класс, присвойте атрибуту **classSchema** **объекта его значение** **true**.</span><span class="sxs-lookup"><span data-stu-id="193b2-117">To disable a class, set the **isDefunct** attribute of its **classSchema** object to **TRUE**.</span></span> <span data-ttu-id="193b2-118">Если класс отключен, новые экземпляры класса создаваться не могут.</span><span class="sxs-lookup"><span data-stu-id="193b2-118">When a class is disabled, new instances of the class cannot be created.</span></span> <span data-ttu-id="193b2-119">Чтобы повторно включить класс, установите для атрибута **уничтожение** значение **false**.</span><span class="sxs-lookup"><span data-stu-id="193b2-119">To re-enable the class set the **isDefunct** attribute to **FALSE**.</span></span>

<span data-ttu-id="193b2-120">Установка объектов схемы как уничтоженных может быть полезна в рабочих средах.</span><span class="sxs-lookup"><span data-stu-id="193b2-120">Setting schema objects as defunct can be useful in production environments.</span></span> <span data-ttu-id="193b2-121">Если тестовая версия расширения схемы больше не требуется, пометьте ее как нефункционирующую.</span><span class="sxs-lookup"><span data-stu-id="193b2-121">When a test version of a schema extension is no longer required, mark it as defunct.</span></span> <span data-ttu-id="193b2-122">Его можно восстановить, удалив атрибут « **уничтожение** » или установив для атрибута значение **false**.</span><span class="sxs-lookup"><span data-stu-id="193b2-122">You can restore it by removing the **isDefunct** attribute or setting the attribute value to **FALSE**.</span></span> <span data-ttu-id="193b2-123">Это также защищает от непреднамеренного удаления объекта схемы, присвоив ему значение уничтоженное, так как операция может быть легко отменена.</span><span class="sxs-lookup"><span data-stu-id="193b2-123">This also protects against an unintended removal of a schema object by setting it to defunct because the operation can be easily reversed.</span></span>

<span data-ttu-id="193b2-124">Имейте в виду, что Active Directory сервер не очищает существующие экземпляры атрибута или класса при уничтожении объекта схемы.</span><span class="sxs-lookup"><span data-stu-id="193b2-124">Be aware that the Active Directory server does not clean up existing instances of an attribute or class when you make a schema object defunct.</span></span> <span data-ttu-id="193b2-125">Если удалить свойство « **уничтожение** », все экземпляры станут допустимыми и нормальными объектами.</span><span class="sxs-lookup"><span data-stu-id="193b2-125">If you remove the **isDefunct** property, any instances become valid, normal objects again.</span></span>

<span data-ttu-id="193b2-126">В следующем списке приведены другие последствия пометки объекта **attributeSchema** или **classSchema** как уничтоженного:</span><span class="sxs-lookup"><span data-stu-id="193b2-126">The following list includes other consequences of marking an **attributeSchema** or **classSchema** object defunct:</span></span>

-   <span data-ttu-id="193b2-127">Добавление или изменение экземпляра завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="193b2-127">Addition or modification of an instance fails.</span></span>
-   <span data-ttu-id="193b2-128">Коды ошибок ведут себя так, как если бы Уничтоженный класс никогда не существовал.</span><span class="sxs-lookup"><span data-stu-id="193b2-128">Error codes behave as if a defunct class never existed.</span></span>
-   <span data-ttu-id="193b2-129">Функции поиска и удаления ведут себя так, как если бы объекты схемы не стали уничтоженными.</span><span class="sxs-lookup"><span data-stu-id="193b2-129">Search and delete behave as if no schema objects have been made defunct.</span></span>
-   <span data-ttu-id="193b2-130">Разрешить удаление всего атрибута из объекта.</span><span class="sxs-lookup"><span data-stu-id="193b2-130">Only allow deleting entire attribute from object.</span></span>

<span data-ttu-id="193b2-131">Следующий список включает дополнительные параметры в рабочей среде для снижения влияния уничтоженных расширений схемы:</span><span class="sxs-lookup"><span data-stu-id="193b2-131">The following list includes additional options in a production environment for reducing the impact of defunct schema extensions:</span></span>

-   <span data-ttu-id="193b2-132">Удалите все значения атрибутов **майхаве** из уничтоженного класса.</span><span class="sxs-lookup"><span data-stu-id="193b2-132">Remove all **mayHave** attribute values from a defunct class.</span></span>
-   <span data-ttu-id="193b2-133">Уменьшите размер всех значений атрибутов **муссаве** из уничтоженного класса.</span><span class="sxs-lookup"><span data-stu-id="193b2-133">Reduce the size of all **mustHave** attribute values from a defunct class.</span></span>
-   <span data-ttu-id="193b2-134">Удаление уничтоженного атрибута из глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="193b2-134">Remove a defunct attribute from the global catalog.</span></span>
-   <span data-ttu-id="193b2-135">Удаляет Уничтоженный атрибут из любого индекса.</span><span class="sxs-lookup"><span data-stu-id="193b2-135">Remove a defunct attribute from any index.</span></span>

<span data-ttu-id="193b2-136">Другие варианты удаления ненужных изменений схемы в рабочей среде — разработчики могут использовать частный контроллер домена для тестирования.</span><span class="sxs-lookup"><span data-stu-id="193b2-136">Other options for removing unwanted schema changes in a production environment are for developers to use a private domain controller for testing.</span></span> <span data-ttu-id="193b2-137">В этом случае можно:</span><span class="sxs-lookup"><span data-stu-id="193b2-137">In this case, you can:</span></span>

-   <span data-ttu-id="193b2-138">Чтобы понизить роль контроллера домена, выполните сброс Active Directory Server с помощью Dcpromo.exe.</span><span class="sxs-lookup"><span data-stu-id="193b2-138">"Reset" the Active Directory server by using Dcpromo.exe to demote the DC.</span></span> <span data-ttu-id="193b2-139">После завершения понижения роли снова используйте Dcpromo.exe, чтобы повысить уровень сервера до контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="193b2-139">After the demote completes, use Dcpromo.exe again to promote the server back to a DC.</span></span> <span data-ttu-id="193b2-140">Затем разработчик может использовать сценарии LDIF для перезагрузки всех требуемых классов, атрибутов и экземпляров объектов.</span><span class="sxs-lookup"><span data-stu-id="193b2-140">The developer can then use LDIF scripts to reload any required classes, attributes, and object instances.</span></span>
-   <span data-ttu-id="193b2-141">Используйте Ntbackup.exe, чтобы выполнить резервное копирование состояния системы в доступном разделе диска.</span><span class="sxs-lookup"><span data-stu-id="193b2-141">Use Ntbackup.exe to perform a system-state backup to an available disk partition.</span></span> <span data-ttu-id="193b2-142">Для восстановления выполните перезагрузку в режим восстановления службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="193b2-142">Reboot to Safe/Directory Service Restore mode to restore.</span></span>

<span data-ttu-id="193b2-143">Для операционных систем Windows Server 2003 при установке класса или атрибута в значение уничтожение можно сразу же повторно использовать значения **LdapDisplayName**, **schemaIdGuid**, **OID** и **mapiID** для уничтоженного элемента схемы при создании нового класса или атрибута для его замены.</span><span class="sxs-lookup"><span data-stu-id="193b2-143">For Windows Server 2003 operating systems, when you set a class or attribute to defunct, you can immediately reuse the **ldapDisplayName**, **schemaIdGuid**, **OID** and **mapiID** values of the defunct schema element when you create a new class or attribute to replace it.</span></span> <span data-ttu-id="193b2-144">Уничтоженная версия класса или атрибута сохраняется в контейнере схемы, но она скрыта в оснастке MMC.</span><span class="sxs-lookup"><span data-stu-id="193b2-144">The defunct version of the class or attribute is maintained in the Schema container, but it is hidden in the MMC snap-in.</span></span> <span data-ttu-id="193b2-145">Чтобы повторно активировать старый элемент схемы **, задайте для** свойства **IsFalse значение false**.</span><span class="sxs-lookup"><span data-stu-id="193b2-145">To reactivate the old schema element, set **isDefunct** to **FALSE**.</span></span>

<span data-ttu-id="193b2-146">В следующем примере кода LDIF показано, как изменить атрибут « **уничтожение** » и изменить RDN так, чтобы он не запутать новый класс, который вы создаете для его замены.</span><span class="sxs-lookup"><span data-stu-id="193b2-146">The following LDIF code example shows how to modify the **isDefunct** attribute and change the RDN so that it is not confused with the new class that you create to replace it.</span></span>

``` syntax
 dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modify
   replace: isDefunct
   isDefunct: TRUE
   -

   dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modrdn
   newrdn: cn=MyClassOld
   deleteoldrdn: 1

   dn:
   changetype: modify
   add: schemaUpdateNow
   schemaUpdateNow: 1
   -
```

<span data-ttu-id="193b2-147">Используйте следующую команду, чтобы выполнить пример кода LDIF в лесу для компьютера, работающего под управлением операционных систем Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="193b2-147">Use the following command to run the LDIF code example against a forest for a computer running on Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="193b2-148">**ldifde/i/f RDN. ldf/c "DC = X" "DC = MyDomain, DC = com"**</span><span class="sxs-lookup"><span data-stu-id="193b2-148">**ldifde /i /f rdn.ldf /c "DC=X" "dc=mydomain,dc=com"**</span></span>

<span data-ttu-id="193b2-149">(Где "DC = X" является константой)</span><span class="sxs-lookup"><span data-stu-id="193b2-149">(Where "DC=X" is a constant)</span></span>

 

 




