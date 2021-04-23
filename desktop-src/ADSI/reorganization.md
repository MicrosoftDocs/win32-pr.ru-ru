---
title: Реорганизации
description: Организация продаж перешла в новую организацию \ 8212; \ 0034; Продажи и поддержка. \ 0034; Джулия Банкерт была выдвинута на вице — президент по интересу и создаст новую организацию.
ms.assetid: 38b05d0b-2739-43c2-aac7-7555a5bfbc91
ms.tgt_platform: multiple
keywords:
- Реорганизация ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587f3de34738814b34ad250bb00bb7b71121d65c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067319"
---
# <a name="reorganization"></a><span data-ttu-id="8c787-105">Реорганизации</span><span class="sxs-lookup"><span data-stu-id="8c787-105">Reorganization</span></span>

<span data-ttu-id="8c787-106">Организация продаж перешла в новую организацию — «продажи и поддержка».</span><span class="sxs-lookup"><span data-stu-id="8c787-106">The sales organization has moved to a new organization — "Sales and Support."</span></span> <span data-ttu-id="8c787-107">Джулия Банкерт была выдвинута на вице — президент по интересу и создаст новую организацию.</span><span class="sxs-lookup"><span data-stu-id="8c787-107">Julie Bankert has been promoted to vice president and will lead the new organization.</span></span> <span data-ttu-id="8c787-108">Джо Ворден, администратор предприятия, должен переместить подразделение «продажи» в новое подразделение, продажи и поддержку.</span><span class="sxs-lookup"><span data-stu-id="8c787-108">Joe Worden, the enterprise administrator, must move Sales OU to a new OU, Sales and Support.</span></span>


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=COM")
Set salesSupport = dom.Create("organizationalUnit", "CN=Sales and Support")
Set sales = salesSupport.MoveHere("LDAP://OU=Sales,DC=Fabrikam,DC=COM", vbNullString)
```



<span data-ttu-id="8c787-109">В этом примере кода все объекты в подразделении Sales, включая подразделение, перемещаются в новое подразделение.</span><span class="sxs-lookup"><span data-stu-id="8c787-109">With this code example, all objects in the sales organizational unit, including the sub-organizational units, are moved to the new organizational unit.</span></span>

<span data-ttu-id="8c787-110">Теперь Сергей может переместить Юлия в подразделение "продажи и поддержка".</span><span class="sxs-lookup"><span data-stu-id="8c787-110">Now, Joe can move Julie into the Sales and Support organizational unit.</span></span>


```VB
Set usr = salesSupport.MoveHere("LDAP://CN=Julie Bankert,OU=Sales,OU=Sales and Support,DC=Fabrikam,DC=COM")
usr.Put "title", "Vice President"
usr.SetInfo
```



<span data-ttu-id="8c787-111">Имейте в виду, что ссылка «руководитель-прямой отчет» между Юлия Банкерт и Олегом серого автоматически обновляется Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8c787-111">Be aware that the manager-direct report link between Julie Bankert and Chris Gray is automatically updated by Active Directory.</span></span>

<span data-ttu-id="8c787-112">**Создание отчета Active Directory**</span><span class="sxs-lookup"><span data-stu-id="8c787-112">**To create an Active Directory report**</span></span>

1.  <span data-ttu-id="8c787-113">Откройте Visual Basic версии 6,0 и при появлении запроса на выбор типа проекта выберите **проект данных**.</span><span class="sxs-lookup"><span data-stu-id="8c787-113">Open Visual Basic version 6.0, and when prompted for the project type, select **Data Project**.</span></span>
2.  <span data-ttu-id="8c787-114">В **проекте данных** дважды щелкните **Environment1 данных**.</span><span class="sxs-lookup"><span data-stu-id="8c787-114">On **Data Project**, double-click **Data Environment1**.</span></span>
3.  <span data-ttu-id="8c787-115">В окне **Среда данных** щелкните правой кнопкой мыши объект подключения **(Connection1)** и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="8c787-115">On the **Data Environment** window, right-click the connection object **(Connection1)** and select **Properties**.</span></span>
4.  <span data-ttu-id="8c787-116">Выберите **поставщик OLE DB для служб каталогов Майкрософт** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="8c787-116">Select **OLE DB Provider for Microsoft Directory Services**, and click **Next**.</span></span>
5.  <span data-ttu-id="8c787-117">Установите флажок **использовать встроенную безопасность Windows NT** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8c787-117">Select **Use Windows NT Integrated security**, and click **OK**.</span></span> <span data-ttu-id="8c787-118">При этом создается объект соединения.</span><span class="sxs-lookup"><span data-stu-id="8c787-118">This creates a connection object.</span></span>
6.  <span data-ttu-id="8c787-119">Снова щелкните правой кнопкой мыши окно **среды данных** , чтобы выбрать **команду Добавить**.</span><span class="sxs-lookup"><span data-stu-id="8c787-119">Right-click the **Data Environment** window again to select **Add Command**.</span></span> <span data-ttu-id="8c787-120">Щелкните правой кнопкой мыши объект **команда1** и выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="8c787-120">Right-click the **Command1** object and select **Properties**.</span></span> <span data-ttu-id="8c787-121">Появится следующее диалоговое окно **свойств команда1** .</span><span class="sxs-lookup"><span data-stu-id="8c787-121">The following **Command1 Properties** dialog box will appear.</span></span>

    ![диалоговое окно «Свойства команда1»](images/adadsi3.png)

7.  <span data-ttu-id="8c787-123">Нажмите кнопку « **инструкция SQL** » и введите следующее:</span><span class="sxs-lookup"><span data-stu-id="8c787-123">Click the **SQL Statement** option button and type the following:</span></span>

    <span data-ttu-id="8c787-124">Выберите имя, telephoneNumber из "LDAP://ДК = Fabrikam, DC = com", где objectCategory = "Person" и objectClass = "User"</span><span class="sxs-lookup"><span data-stu-id="8c787-124">SELECT Name,telephoneNumber FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectCategory='Person' AND objectClass='user'</span></span>

    <span data-ttu-id="8c787-125">Объект **команды** создан.</span><span class="sxs-lookup"><span data-stu-id="8c787-125">The **Command** object is created.</span></span> <span data-ttu-id="8c787-126">Добавьте в отчет объект **Command** .</span><span class="sxs-lookup"><span data-stu-id="8c787-126">Add the **Command** object to the report.</span></span>

8.  <span data-ttu-id="8c787-127">Дважды щелкните **Report1 данных** в окне **проекта** .</span><span class="sxs-lookup"><span data-stu-id="8c787-127">Double-click **Data Report1** from the **Project** window.</span></span>
9.  <span data-ttu-id="8c787-128">Перетащите объект **команда1** из окна **DataEnvironment1** в раздел **сведений** в окне **отчета данных** .</span><span class="sxs-lookup"><span data-stu-id="8c787-128">Drag the **Command1** object from the **DataEnvironment1** window to the **Detail** section in the **Data Report** window.</span></span>
10. <span data-ttu-id="8c787-129">В **свойствах DataReport1** для **DataSource** выберите **DataEnvironment1** в раскрывающемся меню и выберите **команда1** в поле **DataMember** .</span><span class="sxs-lookup"><span data-stu-id="8c787-129">On **DataReport1 Properties**, for **DataSource**, select **DataEnvironment1** from the pull-down menu, and select **Command1** in the **DataMember** field.</span></span>
11. <span data-ttu-id="8c787-130">В окне проекта щелкните правой кнопкой мыши **проект Data** и выберите **Свойства проекта** данных.</span><span class="sxs-lookup"><span data-stu-id="8c787-130">On the project window, right-click **Data Project**, and select **DataProject Properties**.</span></span>
12. <span data-ttu-id="8c787-131">В диалоговом окне " **проект-свойства** проекта" в разделе " **объект запуска**" выберите **DataReport1** в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="8c787-131">On the **DataProject - Project Properties** dialog window, under **Startup Object**, select **DataReport1** from the pull-down menu.</span></span> <span data-ttu-id="8c787-132">Нажмите кнопку **ОК**, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="8c787-132">Click **OK** to save.</span></span>
13. <span data-ttu-id="8c787-133">Компиляция.</span><span class="sxs-lookup"><span data-stu-id="8c787-133">Compile.</span></span> <span data-ttu-id="8c787-134">Появится следующее диалоговое окно **DataReport1** .</span><span class="sxs-lookup"><span data-stu-id="8c787-134">The following **DataReport1** dialog box will appear.</span></span>

    ![диалоговое окно «datareport1»](images/adadsi4.png)

## <a name="related-topics"></a><span data-ttu-id="8c787-136">См. также</span><span class="sxs-lookup"><span data-stu-id="8c787-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c787-137">Соединение разнородных данных</span><span class="sxs-lookup"><span data-stu-id="8c787-137">Joining Heterogeneous Data</span></span>](joining-heterogeneous-data.md)
</dt> </dl>

 

 




