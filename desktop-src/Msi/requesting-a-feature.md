---
description: Существует несколько функций, которые приложение должно вызвать для запроса функций.
ms.assetid: 5253c6f0-316f-4f24-b0c0-951db8d16745
title: Запрос функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5261aac69ad2dd604a072e4b02e3bcde76a2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081024"
---
# <a name="requesting-a-feature"></a><span data-ttu-id="70101-103">Запрос функции</span><span class="sxs-lookup"><span data-stu-id="70101-103">Requesting a Feature</span></span>

<span data-ttu-id="70101-104">Существует несколько функций, которые приложение должно вызвать для запроса функций.</span><span class="sxs-lookup"><span data-stu-id="70101-104">There are several functions an application must call to request features.</span></span> <span data-ttu-id="70101-105">Перед запросом функции приложение должно убедиться, что эта функция установлена.</span><span class="sxs-lookup"><span data-stu-id="70101-105">Before requesting a feature, the application must ensure that the feature is installed.</span></span> <span data-ttu-id="70101-106">Если приложение вызывает [**мсиусефеатуре**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) до того, как приложение обращается к функции, приложение может использовать полученные сведения для поддержки метрик использования.</span><span class="sxs-lookup"><span data-stu-id="70101-106">If the application calls [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) before the application accesses a feature, the application can use the information returned to maintain usage metrics.</span></span>

<span data-ttu-id="70101-107">**Запрос функции**</span><span class="sxs-lookup"><span data-stu-id="70101-107">**To request a feature**</span></span>

1.  <span data-ttu-id="70101-108">Вызовите функцию [**мсиенумфеатурес**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) или [**мсикуерифеатурестате**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) , если требуется определить доступность компонента без увеличения числа использований.</span><span class="sxs-lookup"><span data-stu-id="70101-108">Call the [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) or the [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) function if you want to determine the availability of a feature without incrementing the usage count.</span></span>
2.  <span data-ttu-id="70101-109">Укажите намерение приложения использовать функцию, вызвав функцию [**мсиусефеатуре**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) .</span><span class="sxs-lookup"><span data-stu-id="70101-109">Indicate your application's intent to use a feature by calling the [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) function.</span></span>
3.  <span data-ttu-id="70101-110">Определите расположение файлов, вызвав функцию [**мсижеткомпонентпас**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) .</span><span class="sxs-lookup"><span data-stu-id="70101-110">Determine file locations by calling the [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) function.</span></span>
4.  <span data-ttu-id="70101-111">Настройте компонент, вызвав функцию [**мсиконфигурефеатуре**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) .</span><span class="sxs-lookup"><span data-stu-id="70101-111">Configure the feature by calling the [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) function.</span></span>
5.  <span data-ttu-id="70101-112">Получите метрики использования, которые приложение может использовать, вызвав функцию [**мсижетфеатуреусаже**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea) .</span><span class="sxs-lookup"><span data-stu-id="70101-112">Obtain usage metrics that your application can use by calling the [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea) function.</span></span>

<span data-ttu-id="70101-113">На следующей схеме показана модель запросов функций.</span><span class="sxs-lookup"><span data-stu-id="70101-113">The following diagram illustrates the feature request model.</span></span>

![<span data-ttu-id="70101-114">модель запроса функций.</span><span class="sxs-lookup"><span data-stu-id="70101-114">feature request model.</span></span> ](images/over2.png)

 

 



