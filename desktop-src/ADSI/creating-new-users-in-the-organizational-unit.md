---
title: Создание новых пользователей в подразделении
description: Терри Адамс был принят на работу в компании Fabrikam Sales. Его прямой отчет — Патрик Хинес.
ms.assetid: bc31ed04-e505-4d64-9fa3-d06af7351db0
ms.tgt_platform: multiple
keywords:
- Создание новых пользователей в подразделении ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c45f9dc91f1c36493a4ae8e1c9bb1a69268c9987
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486565"
---
# <a name="creating-new-users-in-the-organizational-unit"></a><span data-ttu-id="c1ef7-105">Создание новых пользователей в подразделении</span><span class="sxs-lookup"><span data-stu-id="c1ef7-105">Creating New Users in the Organizational Unit</span></span>

<span data-ttu-id="c1ef7-106">Терри Адамс был принят на работу в компании Fabrikam Sales.</span><span class="sxs-lookup"><span data-stu-id="c1ef7-106">Terry Adams was hired into the Fabrikam Sales organization.</span></span> <span data-ttu-id="c1ef7-107">Его прямой отчет — Патрик Хинес.</span><span class="sxs-lookup"><span data-stu-id="c1ef7-107">His direct report is Patrick Hines.</span></span>

<span data-ttu-id="c1ef7-108">Как показано в следующем примере кода, Джо Новиков, администратор предприятия, создаст для него новую учетную запись.</span><span class="sxs-lookup"><span data-stu-id="c1ef7-108">As shown in the following code example, Joe Andreshak, the enterprise administrator, will create a new account for him.</span></span>


```VB
Dim salesOU as IADsContainer
Set salesOU = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set usr = salesOU.Create("user", "CN=Terry Adams")
usr.Put "sAMAccountName", "terryadams"
usr.Put "userPrincipalName", "terryadams@fabrikam.com" 
usr.Put "title" "Marketing Manager"
usr.SetInfo

usr.SetPassword "seahorse"
usr.AccountDisabled = False
usr.SetInfo
```



<span data-ttu-id="c1ef7-109">При создании нового пользователя необходимо указать **SamAccountName**.</span><span class="sxs-lookup"><span data-stu-id="c1ef7-109">When creating a new user, you must specify a **sAMAccountName**.</span></span> <span data-ttu-id="c1ef7-110">Это обязательный атрибут для класса User.</span><span class="sxs-lookup"><span data-stu-id="c1ef7-110">This is a mandatory attribute for the user class.</span></span> <span data-ttu-id="c1ef7-111">Прежде чем можно будет создать экземпляр объекта, необходимо задать все обязательные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="c1ef7-111">Before an instance of an object can be created, all mandatory attributes must be set.</span></span> <span data-ttu-id="c1ef7-112">**SamAccountName** будет автоматически сформирован, если он не указан для нового пользователя.</span><span class="sxs-lookup"><span data-stu-id="c1ef7-112">The **sAMAccountName** will automatically be generated if one is not specified for a new user.</span></span>

<span data-ttu-id="c1ef7-113">При создании нового пользователя все необходимые атрибуты должны быть установлены в локальном кэше перед вызовом метода [**iAds. сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="c1ef7-113">When creating a new user, all of the required attributes must be set in the local cache before the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method is called.</span></span>

<span data-ttu-id="c1ef7-114">Джо, как администратор, может назначить пароль Терри с помощью метода [**IADsUser. SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) .</span><span class="sxs-lookup"><span data-stu-id="c1ef7-114">Joe, as an administrator, can assign Terry's password using the [**IADsUser.SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) method.</span></span> <span data-ttu-id="c1ef7-115">Метод **IADsUser. SetPassword** не будет работать до вызова метода [**iAds. сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="c1ef7-115">The **IADsUser.SetPassword** method will not work until the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method has been called.</span></span>

<span data-ttu-id="c1ef7-116">Затем Сергей включает учетную запись пользователя, присвоив свойству [**IADsUser. Аккаунтдисаблед**](iadsuser-property-methods.md) **значение false**.</span><span class="sxs-lookup"><span data-stu-id="c1ef7-116">Then, Joe enables the user account by setting the [**IADsUser.AccountDisabled**](iadsuser-property-methods.md) property to **FALSE**.</span></span>

<span data-ttu-id="c1ef7-117">В следующем примере кода показано, как задать Терри в качестве менеджера Патрик.</span><span class="sxs-lookup"><span data-stu-id="c1ef7-117">The following code example shows how to set Terry as Patrick's manager.</span></span>


```VB
Set usr = GetObject("LDAP://CN=patrickhines,OU=Sales,DC=Fabrikam,DC=COM")
usr.Put "manager", "CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM"
usr.SetInfo
```



<span data-ttu-id="c1ef7-118">Может возникнуть вопрос, что произойдет, если Терри изменит свое имя, перейдет в другую организацию или покидает компанию.</span><span class="sxs-lookup"><span data-stu-id="c1ef7-118">You may wonder what happens if Terry changes his name, moves to a different organization, or leaves the company.</span></span> <span data-ttu-id="c1ef7-119">Кто обслуживает связь «руководитель — прямой отчет»?</span><span class="sxs-lookup"><span data-stu-id="c1ef7-119">Who maintains this manager-direct report link?</span></span> <span data-ttu-id="c1ef7-120">Дополнительные сведения и решение этой проблемы см. в разделе [reorganization](reorganization.md).</span><span class="sxs-lookup"><span data-stu-id="c1ef7-120">For more information, and the solution to this problem, see [Reorganization](reorganization.md).</span></span> <span data-ttu-id="c1ef7-121">Поскольку схема Active Directory является расширяемой, вы можете моделировать объекты для включения аналогичных связей между руководителями и подчиненными стилями.</span><span class="sxs-lookup"><span data-stu-id="c1ef7-121">Because the Active Directory schema is extensible, you can model your objects to include similar manager-direct report style relationships.</span></span>

<span data-ttu-id="c1ef7-122">Прежде чем перейти к следующей задаче, Взгляните на пример кода, демонстрирующий, как Сергей будет просматривать непосредственные подчиненные отчеты Терри.</span><span class="sxs-lookup"><span data-stu-id="c1ef7-122">Before going on to the next task, look at a code example that shows how Joe would view Terry's direct reports.</span></span>


```VB
Set usr = GetObject("LDAP://CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM")
reports = usr.GetEx ("directReports")

For each directReport in reports
    Debug.Print directReport
Next
```



<span data-ttu-id="c1ef7-123">В этом примере кода Патрик будет отображаться как прямой отчет Терри, даже если атрибут **directReports** никогда не изменялся.</span><span class="sxs-lookup"><span data-stu-id="c1ef7-123">In this code example, Patrick will display as Terry's direct report, even though the **directReports** attribute was never modified.</span></span> <span data-ttu-id="c1ef7-124">Active Directory выполняет это автоматически.</span><span class="sxs-lookup"><span data-stu-id="c1ef7-124">Active Directory does this automatically.</span></span>

<span data-ttu-id="c1ef7-125">В мире каталога атрибут может иметь одно или несколько значений.</span><span class="sxs-lookup"><span data-stu-id="c1ef7-125">In the directory world, an attribute can have single or multiple values.</span></span> <span data-ttu-id="c1ef7-126">Поскольку **directReports** имеет несколько значений, эти сведения можно получить, просмотрев схему, проще использовать метод [**iAds. жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) , который возвращает массив значений независимо от того, возвращено ли одно или несколько значений.</span><span class="sxs-lookup"><span data-stu-id="c1ef7-126">Because **directReports** has multiple values, you can get this information by looking at the schema, it is easier to use the [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method, which returns an array of values regardless of whether single or multiple values are returned.</span></span>

<span data-ttu-id="c1ef7-127">Оснастка Active Directory пользователи и компьютеры позволяет просматривать непосредственные связи между отчетами и менеджерами на странице свойств пользователя.</span><span class="sxs-lookup"><span data-stu-id="c1ef7-127">The Active Directory Users and Computers snap-in lets you view direct reports and manager relationships on the user's property page.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1ef7-128">См. также</span><span class="sxs-lookup"><span data-stu-id="c1ef7-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1ef7-129">Добавление пользователей в группу</span><span class="sxs-lookup"><span data-stu-id="c1ef7-129">Adding Users to a Group</span></span>](adding-users-to-a-group.md)
</dt> </dl>

 

 




