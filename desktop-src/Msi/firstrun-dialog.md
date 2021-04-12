---
description: Последовательность диалоговых окон файла firstrun собирает сведения об имени пользователя, имени компании и ИДЕНТИФИКАТОРе продукта. В этом диалоговом окне установщик проверяет идентификатор продукта.
ms.assetid: bb77296f-705a-4409-b2ca-a76bbaf7ea57
title: Диалоговое окно файла firstrun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2024683d7a10395340a18ddd2015b94e1207bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263603"
---
# <a name="firstrun-dialog"></a><span data-ttu-id="d6018-104">Диалоговое окно файла firstrun</span><span class="sxs-lookup"><span data-stu-id="d6018-104">FirstRun Dialog</span></span>

<span data-ttu-id="d6018-105">Последовательность диалоговых окон файла firstrun собирает сведения об имени пользователя, имени компании и ИДЕНТИФИКАТОРе продукта.</span><span class="sxs-lookup"><span data-stu-id="d6018-105">A FirstRun dialog box sequence collects user name, company name, and product ID information.</span></span> <span data-ttu-id="d6018-106">В этом диалоговом окне установщик проверяет идентификатор продукта.</span><span class="sxs-lookup"><span data-stu-id="d6018-106">The installer verifies the product ID during this dialog.</span></span>

<span data-ttu-id="d6018-107">Последовательность диалоговых окон файла firstrun обычно не является частью последовательности действий и вызывается функцией [**мсиколлектусеринфо**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) при первом запуске продукта.</span><span class="sxs-lookup"><span data-stu-id="d6018-107">A FirstRun dialog box sequence is usually not a part of the action sequence and is instead called by the [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) function on the first run of the product.</span></span>

<span data-ttu-id="d6018-108">Автор пакета установщика может использовать последовательность диалогового окна шаблона или создать другую последовательность.</span><span class="sxs-lookup"><span data-stu-id="d6018-108">An author of an installer package may use the template dialog sequence or create a different sequence.</span></span> <span data-ttu-id="d6018-109">Однако для последовательности диалоговых окон необходимо, чтобы пользователь установил следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="d6018-109">The dialog sequence however needs to have the user set the following properties:</span></span>

-   <span data-ttu-id="d6018-110">Свойство [**username**](username.md)</span><span class="sxs-lookup"><span data-stu-id="d6018-110">[**USERNAME**](username.md) property</span></span>
-   <span data-ttu-id="d6018-111">[**COMPANYNAME**](companyname.md) , свойство</span><span class="sxs-lookup"><span data-stu-id="d6018-111">[**COMPANYNAME**](companyname.md) property</span></span>
-   <span data-ttu-id="d6018-112">[**PIDKEY**](pidkey.md) , свойство</span><span class="sxs-lookup"><span data-stu-id="d6018-112">[**PIDKEY**](pidkey.md) property</span></span>

<span data-ttu-id="d6018-113">Идентификатор продукта будет проверяться в диалоговом окне с помощью [действия валидатепродуктид](validateproductid-action.md) или [валидатепродуктид таблице ControlEvent событие](validateproductid-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="d6018-113">The product ID will be validated during the dialog using the [ValidateProductID action](validateproductid-action.md) or the [ValidateProductID ControlEvent](validateproductid-controlevent.md).</span></span>

<span data-ttu-id="d6018-114">Если идентификатор продукта установлен в качестве свойства в командной строке или при преобразовании, то необходимость в повторном вводе идентификатора продукта в диалоговом окне первого запуска можно обойти, управляя отображением с помощью свойства [**ProductID**](productid.md) .</span><span class="sxs-lookup"><span data-stu-id="d6018-114">If the product ID is set as a property on the command line, or by a transform, then the necessity of having the user reenter the product ID during the first-run dialog can be circumvented by controlling the display using the [**ProductID**](productid.md) property.</span></span> <span data-ttu-id="d6018-115">После успешной проверки идентификатора продукта свойству **ProductID** присваивается полный, допустимый идентификатор продукта.</span><span class="sxs-lookup"><span data-stu-id="d6018-115">Following the successful validation of the product ID the **ProductID** property is set to the full, valid product ID.</span></span>

 

 



