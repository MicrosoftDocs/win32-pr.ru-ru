---
description: База данных продуктов содержит сведения о продукте. Дополнительные сведения о получении сведений о продукте с помощью функций перечисления см. в разделе Инициализация приложения.
ms.assetid: 528c915c-296c-4620-8105-0b5d543e56a5
title: Получение сведений о приложении
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dce842f057efb65b6d0db3ad0407a19bf08435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991456"
---
# <a name="getting-application-information"></a><span data-ttu-id="4b995-104">Получение сведений о приложении</span><span class="sxs-lookup"><span data-stu-id="4b995-104">Getting Application Information</span></span>

<span data-ttu-id="4b995-105">База данных продуктов содержит сведения о продукте.</span><span class="sxs-lookup"><span data-stu-id="4b995-105">The product database contains information about a product.</span></span> <span data-ttu-id="4b995-106">Дополнительные сведения о получении сведений о продукте с помощью функций перечисления см. в разделе [Инициализация приложения](initializing-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="4b995-106">For more information on obtaining product information with enumeration functions, see [Initializing an Application](initializing-an-application.md).</span></span>

<span data-ttu-id="4b995-107">**Получение сведений о продукте**</span><span class="sxs-lookup"><span data-stu-id="4b995-107">**To get product information**</span></span>

1.  <span data-ttu-id="4b995-108">Убедитесь, что продукт установлен путем вызова функции [**мсикуерипродуктстате**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea) .</span><span class="sxs-lookup"><span data-stu-id="4b995-108">Verify that a product is installed by calling the [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea) function.</span></span>
2.  <span data-ttu-id="4b995-109">Откройте базу данных и получите в ней маркер, вызвав функцию [**мсиопенпродукт**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) .</span><span class="sxs-lookup"><span data-stu-id="4b995-109">Open the database and obtain a handle to it by calling the [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) function.</span></span>

    <span data-ttu-id="4b995-110">Если база данных содержится в установочном пакете, вызовите функцию [**мсиопенпаккаже**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea) .</span><span class="sxs-lookup"><span data-stu-id="4b995-110">If the database is contained in an installation package, call the [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea) function.</span></span>

3.  <span data-ttu-id="4b995-111">Используйте открытый дескриптор для получения свойств продукта с помощью функции [**мсижетпродуктпроперти**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya) , а также для получения описательных сведений о функции с помощью функции [**мсижетфеатуреинфо**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa) .</span><span class="sxs-lookup"><span data-stu-id="4b995-111">Use the open handle to obtain product properties with the [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya) function, and to obtain descriptive feature information with the [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa) function.</span></span>

    <span data-ttu-id="4b995-112">Если требуется получить сведения о продукте с помощью кода продукта, а не с помощью открытого обработчика базы данных, вызовите функцию [**мсижетпродуктинфо**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) вместо [**мсижетпродуктпроперти**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya).</span><span class="sxs-lookup"><span data-stu-id="4b995-112">If you want to obtain product information using the product code, rather than using the open database handle, call the [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) function instead of [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya).</span></span>

4.  <span data-ttu-id="4b995-113">Закройте открытый обработчик установки, вызвав функцию [**мсиклосехандле**](/windows/desktop/api/Msi/nf-msi-msiclosehandle) .</span><span class="sxs-lookup"><span data-stu-id="4b995-113">Close an open installation handle by calling the [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle) function.</span></span>

    <span data-ttu-id="4b995-114">Функция [**мсиклосеаллхандлес**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) является диагностической функцией и не должна использоваться для закрытия дескрипторов, которые вы должны открыть.</span><span class="sxs-lookup"><span data-stu-id="4b995-114">The [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) function is a diagnostic function and should not be used to close handles you know to be open.</span></span> <span data-ttu-id="4b995-115">Можно вызвать функцию **мсиклосеаллхандлес** при закрытии приложения, чтобы убедиться, что все дескрипторы закрыты.</span><span class="sxs-lookup"><span data-stu-id="4b995-115">It is acceptable to call the **MsiCloseAllHandles** function when the application closes to ensure that all handles have been closed.</span></span>

 

 



