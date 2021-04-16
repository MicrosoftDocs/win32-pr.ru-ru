---
description: Вы можете установить все продукты с помощью функций установщик Windows. Ниже описана процедура установки продукта.
ms.assetid: 03cc7abc-63bd-4a01-a05c-9f7928de8827
title: Установка приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf312e7394c4fcbca699f6e032e315a42356c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664315"
---
# <a name="installing-an-application"></a><span data-ttu-id="d7c41-104">Установка приложения</span><span class="sxs-lookup"><span data-stu-id="d7c41-104">Installing an Application</span></span>

<span data-ttu-id="d7c41-105">Вы можете установить все продукты с помощью функций установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="d7c41-105">You can install entire products with Windows Installer functions.</span></span> <span data-ttu-id="d7c41-106">Ниже описана процедура установки продукта.</span><span class="sxs-lookup"><span data-stu-id="d7c41-106">The following steps describe how to install a product.</span></span>

<span data-ttu-id="d7c41-107">**Установка продукта**</span><span class="sxs-lookup"><span data-stu-id="d7c41-107">**To install a product**</span></span>

1.  <span data-ttu-id="d7c41-108">Запустите продукт через его установку или последовательность удаления, вызвав функцию [**мсиинсталлпродукт**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) .</span><span class="sxs-lookup"><span data-stu-id="d7c41-108">Run a product through its installation or uninstallation sequence by calling the [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) function.</span></span>
2.  <span data-ttu-id="d7c41-109">Укажите уровень установки, вызвав функцию [**мсиконфигурепродукт**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) .</span><span class="sxs-lookup"><span data-stu-id="d7c41-109">Specify the installation level by calling the [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) function.</span></span>

    <span data-ttu-id="d7c41-110">Для установки состояния установки можно использовать параметры функции [**мсиконфигурепродукт**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) .</span><span class="sxs-lookup"><span data-stu-id="d7c41-110">You can use the parameters of the [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) function to set the installation state.</span></span> <span data-ttu-id="d7c41-111">Например, можно задать для состояния значение установить локально или установить из источника.</span><span class="sxs-lookup"><span data-stu-id="d7c41-111">For example, you can set the state to install locally or to install from the source.</span></span> <span data-ttu-id="d7c41-112">Вы можете задать диапазон компонентов продукта, который будет включен, задав уровень.</span><span class="sxs-lookup"><span data-stu-id="d7c41-112">You can set the range of product features to be included by setting the level.</span></span>

<span data-ttu-id="d7c41-113">Дополнительные сведения об установке приложения см. в разделе механизм [устойчивости](resiliency.md) и [установки](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="d7c41-113">For more information about installing an application, see [Resiliency](resiliency.md) and [Installation Mechanism](installation-mechanism.md).</span></span>

 

 



