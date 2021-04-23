---
description: 'Когда приложение выполняет операцию Ипропертистораже:: Вритемултипле для любого записываемого свойства получения образа Windows (WIA), драйвер WIA выполняет проверку нового значения свойства.'
ms.assetid: 61ab2b8b-4c0a-40f4-87f0-2dd3ceea70ab
title: Проверка свойства WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60d9e64122e19249c19bc47564631162d783920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263119"
---
# <a name="wia-property-validation"></a><span data-ttu-id="15c69-103">Проверка свойства WIA</span><span class="sxs-lookup"><span data-stu-id="15c69-103">WIA Property Validation</span></span>

<span data-ttu-id="15c69-104">Когда приложение выполняет операцию [ипропертистораже:: вритемултипле](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) для любого записываемого свойства получения образа Windows (WIA), драйвер WIA выполняет проверку нового значения свойства.</span><span class="sxs-lookup"><span data-stu-id="15c69-104">When an application performs an [IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) operation on any writeable Windows Image Acquisition (WIA) property, the WIA driver performs a validation on the new property value.</span></span> <span data-ttu-id="15c69-105">Запись одного свойства может повлиять на изменение других значений свойств.</span><span class="sxs-lookup"><span data-stu-id="15c69-105">Writing one property may have side affects that change other property values.</span></span> <span data-ttu-id="15c69-106">Приложение считывает все значения свойств после операции записи, чтобы определить, что для всех свойств задано значение, необходимое для приложения.</span><span class="sxs-lookup"><span data-stu-id="15c69-106">It is up to the application to read all property values after a write operation to determine that all properties are set to values the application desires.</span></span>

<span data-ttu-id="15c69-107">Несколько свойств можно записать одновременно с помощью операции [ипропертистораже:: вритемултипле](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) .</span><span class="sxs-lookup"><span data-stu-id="15c69-107">Multiple properties can be written simultaneously using the [IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) operation.</span></span> <span data-ttu-id="15c69-108">Возможны случаи, когда некоторые назначения свойств конфликтуют.</span><span class="sxs-lookup"><span data-stu-id="15c69-108">There may be cases where some property assignments conflict.</span></span> <span data-ttu-id="15c69-109">В таких случаях приоритет разрешения конфликтов используется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="15c69-109">In such cases, the priority used to resolve conflicts is as follows:</span></span>

1.  <span data-ttu-id="15c69-110">выявляются \_ IP-адреса с \_ \_ целью по WIA</span><span class="sxs-lookup"><span data-stu-id="15c69-110">WIA\_IPS\_CUR\_INTENT</span></span>
2.  <span data-ttu-id="15c69-111">\_ \_ тип данных WIA IPA</span><span class="sxs-lookup"><span data-stu-id="15c69-111">WIA\_IPA\_DATATYPE</span></span>
3.  <span data-ttu-id="15c69-112">\_глубина IPA \_ WIA</span><span class="sxs-lookup"><span data-stu-id="15c69-112">WIA\_IPA\_DEPTH</span></span>
4.  <span data-ttu-id="15c69-113">\_ксрес IP-адресов WIA \_</span><span class="sxs-lookup"><span data-stu-id="15c69-113">WIA\_IPS\_XRES</span></span>
5.  <span data-ttu-id="15c69-114">\_ирес IP-адресов WIA \_</span><span class="sxs-lookup"><span data-stu-id="15c69-114">WIA\_IPS\_YRES</span></span>
6.  <span data-ttu-id="15c69-115">\_кспос IP-адресов WIA \_</span><span class="sxs-lookup"><span data-stu-id="15c69-115">WIA\_IPS\_XPOS</span></span>
7.  <span data-ttu-id="15c69-116">\_ИПОС IP-адресов WIA \_</span><span class="sxs-lookup"><span data-stu-id="15c69-116">WIA\_IPS\_YPOS</span></span>
8.  <span data-ttu-id="15c69-117">\_ксекстент IP-адресов WIA \_</span><span class="sxs-lookup"><span data-stu-id="15c69-117">WIA\_IPS\_XEXTENT</span></span>
9.  <span data-ttu-id="15c69-118">\_екстент IP-адресов WIA \_</span><span class="sxs-lookup"><span data-stu-id="15c69-118">WIA\_IPS\_YEXTENT</span></span>

## <a name="related-topics"></a><span data-ttu-id="15c69-119">См. также</span><span class="sxs-lookup"><span data-stu-id="15c69-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15c69-120">**ивиапропертистораже**</span><span class="sxs-lookup"><span data-stu-id="15c69-120">**IWiaPropertyStorage**</span></span>](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)
</dt> </dl>

 

 
