---
title: Расширение схемы
description: Если существующие классы и (или) атрибуты не соответствуют типу данных, которые необходимо сохранить, может потребоваться расширение схемы.
ms.assetid: 9a80ce29-8ff0-4324-8a2f-afd6c5d2272e
ms.tgt_platform: multiple
keywords:
- Схема AD, расширение
- Active Directory, использование, схема
- Active Directory, использование, схема, расширение схемы, расширение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437b23229182e6ec6f94b500feb764b4bbcf06e7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789522"
---
# <a name="how-to-extend-the-schema"></a><span data-ttu-id="36cf9-106">Расширение схемы</span><span class="sxs-lookup"><span data-stu-id="36cf9-106">How to Extend the Schema</span></span>

<span data-ttu-id="36cf9-107">Если существующие классы и (или) атрибуты не соответствуют типу данных, которые необходимо сохранить, может потребоваться расширение схемы.</span><span class="sxs-lookup"><span data-stu-id="36cf9-107">When the existing classes and/or attributes do not fit with the type of data that you want to store, you might want to extend the schema.</span></span> <span data-ttu-id="36cf9-108">Дополнительные сведения о принятии решения о том, когда следует расширять схему, см. [в разделе Расширение схемы](extending-the-schema.md).</span><span class="sxs-lookup"><span data-stu-id="36cf9-108">For more information on deciding when to extend the schema, see [Extending the Schema](extending-the-schema.md).</span></span> <span data-ttu-id="36cf9-109">Когда вы решили, что расширение схемы является обязательным, используйте следующую процедуру для расширения схемы.</span><span class="sxs-lookup"><span data-stu-id="36cf9-109">When you have decided that schema extension is required, use the following procedure to extend the schema.</span></span>

## <a name="verify-active-directory-functionality-before-you-apply-any-schema-extensions"></a><span data-ttu-id="36cf9-110">Проверка функциональности Active Directory перед применением любых расширений схемы</span><span class="sxs-lookup"><span data-stu-id="36cf9-110">Verify Active Directory functionality before you apply any schema extensions</span></span>

<span data-ttu-id="36cf9-111">Перед обновлением схемы убедитесь, Active Directory функциональные возможности, чтобы обеспечить продолжение расширения схемы без ошибок.</span><span class="sxs-lookup"><span data-stu-id="36cf9-111">Verify Active Directory functionality before you update the schema to help ensure that the schema extension proceeds without error.</span></span> <span data-ttu-id="36cf9-112">Как минимум убедитесь, что все контроллеры домена для леса подключены к сети и выполняют входящую репликацию.</span><span class="sxs-lookup"><span data-stu-id="36cf9-112">At a minimum, ensure that all domain controllers for the forest are online and performing inbound replication.</span></span>

<span data-ttu-id="36cf9-113">**Проверка функциональности Active Directory перед применением расширения схемы**</span><span class="sxs-lookup"><span data-stu-id="36cf9-113">**To verify Active Directory functionality before you apply the schema extension**</span></span>

1.  <span data-ttu-id="36cf9-114">Войдите на рабочую станцию администратора, на которой Repadmin.exe установлен инструмент поддержки Windows.</span><span class="sxs-lookup"><span data-stu-id="36cf9-114">Log on to an administrative workstation that has the Windows Support Tool Repadmin.exe installed.</span></span>
    > [!Note]  
    > <span data-ttu-id="36cf9-115">Средства поддержки находятся на установочном носителе операционной системы в \\ папке средства поддержки.</span><span class="sxs-lookup"><span data-stu-id="36cf9-115">The Support Tools are located on the operating system installation media in the Support\\Tools folder.</span></span>

     

2.  <span data-ttu-id="36cf9-116">Откройте командную строку, а затем измените каталоги на папку, в которой установлены средства поддержки Windows.</span><span class="sxs-lookup"><span data-stu-id="36cf9-116">Open a command prompt, and then change directories to the folder in which the Windows Support Tools are installed.</span></span>
3.  <span data-ttu-id="36cf9-117">В командной строке введите следующую команду и нажмите клавишу ВВОД:</span><span class="sxs-lookup"><span data-stu-id="36cf9-117">At a command prompt, type the following, and then press ENTER:</span></span>

    ``` syntax
    repadmin /replsum /bysrc /bydest /sort:delta
    ```

    <span data-ttu-id="36cf9-118">Все контроллеры домена должны показывать 0 в столбце "сбой", а самые крупные разности (которые указывают число изменений, внесенных в базу данных Active Directory с момента последней успешной репликации), должны быть меньше или приблизительно равны частоте репликации связи сайтов, используемой контроллером домена для репликации.</span><span class="sxs-lookup"><span data-stu-id="36cf9-118">All domain controllers should show 0 in the Fails column, and the largest deltas (which indicate the number of changes that have been made to the Active Directory database since the last successful replication) should be less than or roughly equal to the replication frequency of the site link that is used by the domain controller for replication.</span></span> <span data-ttu-id="36cf9-119">Периодичность репликации по умолчанию составляет 180 минут.</span><span class="sxs-lookup"><span data-stu-id="36cf9-119">The default replication frequency is 180 minutes.</span></span>

    <span data-ttu-id="36cf9-120">Дополнительные сведения о дополнительных действиях, которые можно предпринять для проверки Active Directory функциональности перед применением расширения схемы, см. [в статье 325379 базы знаний Майкрософт](https://support.microsoft.com/kb/325379/en-us).</span><span class="sxs-lookup"><span data-stu-id="36cf9-120">For more information about additional steps that you can take to verify Active Directory functionality before you apply the schema extension, see [article 325379 in the Microsoft Knowledge Base](https://support.microsoft.com/kb/325379/en-us).</span></span>

<span data-ttu-id="36cf9-121">**Расширение схемы**</span><span class="sxs-lookup"><span data-stu-id="36cf9-121">**To Extend the Schema**</span></span>

1.  <span data-ttu-id="36cf9-122">Определите метод расширения.</span><span class="sxs-lookup"><span data-stu-id="36cf9-122">Determine the method of extension.</span></span> <span data-ttu-id="36cf9-123">После тщательного создания изменений схемы необходимо решить, какой метод следует использовать для расширения схемы.</span><span class="sxs-lookup"><span data-stu-id="36cf9-123">Once you have carefully designed your schema changes, the next step is to decide which method to use to extend the schema.</span></span> <span data-ttu-id="36cf9-124">Можно использовать один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="36cf9-124">You can use one of the following methods:</span></span>
    -   <span data-ttu-id="36cf9-125">Вручную, используя файлы импорта.</span><span class="sxs-lookup"><span data-stu-id="36cf9-125">Manually, using import files.</span></span> <span data-ttu-id="36cf9-126">См. документацию [с помощью средства Ldifde](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65)).</span><span class="sxs-lookup"><span data-stu-id="36cf9-126">See the documentation [Using the LDIFDE Tool](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65)).</span></span>
        > [!Note]  
        > <span data-ttu-id="36cf9-127">Не используйте LDIFDE для импорта файлов Windows SCH \* . ldf.</span><span class="sxs-lookup"><span data-stu-id="36cf9-127">Do not use LDIFDE to import Windows Sch\*.ldf files.</span></span> <span data-ttu-id="36cf9-128">Эти файлы необходимы для расширения схемы Active Directory, чтобы установить контроллеры домена под управлением более новой версии Windows Server, чем версия, запущенная на текущем хозяине схемы.</span><span class="sxs-lookup"><span data-stu-id="36cf9-128">Those files are required to extend the Active Directory schema in order to install domain controllers that run a newer version of Windows Server than the version that is running on the current schema master.</span></span> <span data-ttu-id="36cf9-129">Если необходимо расширить схему для установки нового контроллера домена, используйте Adprep.exe.</span><span class="sxs-lookup"><span data-stu-id="36cf9-129">When you need to extend the schema in order to install a new domain controller, use Adprep.exe.</span></span>

         

    -   <span data-ttu-id="36cf9-130">Программно, с помощью программы установки.</span><span class="sxs-lookup"><span data-stu-id="36cf9-130">Programmatically, using an installation program.</span></span> <span data-ttu-id="36cf9-131">Дополнительные сведения см. в разделе [программное расширение](programmatic-extension.md) .</span><span class="sxs-lookup"><span data-stu-id="36cf9-131">For more information, see [Programmatic Extension](programmatic-extension.md)</span></span>
2.  <span data-ttu-id="36cf9-132">Включение изменений схемы.</span><span class="sxs-lookup"><span data-stu-id="36cf9-132">Enable Schema Changes.</span></span> <span data-ttu-id="36cf9-133">Дополнительные сведения см. в разделе [Предварительные требования для установки расширения схемы](prerequisites-for-installing-a-schema-extension.md) и [включения изменений схемы в хозяине схемы](enabling-schema-changes-at-the-schema-master.md).</span><span class="sxs-lookup"><span data-stu-id="36cf9-133">For more information, see [Prerequisites for Installing a Schema Extension](prerequisites-for-installing-a-schema-extension.md) and [Enabling Schema Changes at the Schema Master](enabling-schema-changes-at-the-schema-master.md).</span></span>
3.  <span data-ttu-id="36cf9-134">Получите идентификатор объекта (OID) для новых атрибутов и (или) классов, как описано в разделе [Получение идентификатора объекта](obtaining-an-object-identifier.md).</span><span class="sxs-lookup"><span data-stu-id="36cf9-134">Obtain an Object Identifier (OID) for your new attributes and/or classes, as described in [Obtaining an Object Identifier](obtaining-an-object-identifier.md).</span></span>
4.  <span data-ttu-id="36cf9-135">Создайте новые атрибуты и классы.</span><span class="sxs-lookup"><span data-stu-id="36cf9-135">Create new attributes and classes.</span></span>
5.  <span data-ttu-id="36cf9-136">При необходимости используйте описатели вывода для интеграции новых атрибутов и классов с пользовательским интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="36cf9-136">Use display specifiers to integrate new attributes and classes with the user interface, if necessary.</span></span>
6.  <span data-ttu-id="36cf9-137">Обновите кэш схемы, как описано в разделе [Обновление кэша схемы](updating-the-schema-cache.md).</span><span class="sxs-lookup"><span data-stu-id="36cf9-137">Update the schema cache as described in [Updating the Schema Cache](updating-the-schema-cache.md).</span></span>
7.  <span data-ttu-id="36cf9-138">Проверьте расширение схемы с помощью LDP.exe.</span><span class="sxs-lookup"><span data-stu-id="36cf9-138">Verify the schema extension using LDP.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36cf9-139">См. также</span><span class="sxs-lookup"><span data-stu-id="36cf9-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36cf9-140">Получение идентификатора объекта</span><span class="sxs-lookup"><span data-stu-id="36cf9-140">Obtaining an Object Identifier</span></span>](obtaining-an-object-identifier.md)
</dt> <dt>

[<span data-ttu-id="36cf9-141">Новые средства командной строки для Active Directory в Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="36cf9-141">The new command-line tools for Active Directory in Windows Server 2003</span></span>](https://support.microsoft.com/kb/298882)
</dt> <dt>

<span data-ttu-id="36cf9-142">[Использование средства LDIFDE](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))</span><span class="sxs-lookup"><span data-stu-id="36cf9-142">[Using the LDIFDE Tool](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))</span></span>
</dt> <dt>

<span data-ttu-id="36cf9-143">[Расширение схемы Active Directory](/previous-versions/ms806972(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="36cf9-143">[Extending the Active Directory Schema](/previous-versions/ms806972(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="36cf9-144">Ограничения на расширение схемы</span><span class="sxs-lookup"><span data-stu-id="36cf9-144">Restrictions on Schema Extension</span></span>](restrictions-on-schema-extension.md)
</dt> </dl>

 

 