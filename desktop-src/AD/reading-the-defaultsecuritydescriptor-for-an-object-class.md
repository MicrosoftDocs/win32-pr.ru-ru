---
title: Чтение Дефаултсекуритидескриптор для класса Object
description: С помощью ADSI можно получить атрибут Дефаултсекуритидескриптор для класса объекта с помощью интерфейса IADs.
ms.assetid: 12d1e77a-bd70-4c64-9b4f-ac5caaf5fe40
ms.tgt_platform: multiple
keywords:
- Active Directory примеры Active Directory, чтение Дефаултсекуритидескриптор для класса Object
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e217ae42214c2c07867c2a57427d74fb7636736
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069752"
---
# <a name="reading-the-defaultsecuritydescriptor-for-an-object-class"></a><span data-ttu-id="4b287-104">Чтение Дефаултсекуритидескриптор для класса Object</span><span class="sxs-lookup"><span data-stu-id="4b287-104">Reading the defaultSecurityDescriptor for an Object Class</span></span>

<span data-ttu-id="4b287-105">С помощью ADSI можно получить атрибут **дефаултсекуритидескриптор** для класса объекта с помощью интерфейса [**iAds**](/windows/desktop/api/iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="4b287-105">Using ADSI, you can obtain the **defaultSecurityDescriptor** attribute for an object class with the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface.</span></span> <span data-ttu-id="4b287-106">Чтобы получить атрибут **дефаултсекуритидескриптор** для класса объекта, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4b287-106">To obtain the **defaultSecurityDescriptor** attribute for an object class, perform the following steps.</span></span>

1.  <span data-ttu-id="4b287-107">Получите указатель интерфейса [**iAds**](/windows/desktop/api/iads/nn-iads-iads) на объект **classSchema** для класса Object.</span><span class="sxs-lookup"><span data-stu-id="4b287-107">Get an [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface pointer to the **classSchema** object for the object class.</span></span>
2.  <span data-ttu-id="4b287-108">Используйте метод [**iAds. Get**](/windows/desktop/api/iads/nf-iads-iads-get) , чтобы получить дескриптор безопасности объекта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4b287-108">Use the [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to get the default security descriptor of the object.</span></span> <span data-ttu-id="4b287-109">Имя свойства, содержащего дескриптор безопасности, — "Дефаултсекуритидескриптор".</span><span class="sxs-lookup"><span data-stu-id="4b287-109">The name of the property that contains the security descriptor is "defaultSecurityDescriptor".</span></span> <span data-ttu-id="4b287-110">Свойство будет возвращено как [**значение типа Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) , содержащее BSTR с дескриптором безопасности по умолчанию в формате строки SDDL.</span><span class="sxs-lookup"><span data-stu-id="4b287-110">The property will be returned as a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) containing a BSTR with the default security descriptor in SDDL string format.</span></span>
3.  <span data-ttu-id="4b287-111">Используйте функцию [**конвертстрингсекуритидескриптортосекуритидескриптор**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) , чтобы преобразовать форму строки SDDL в дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="4b287-111">Use the [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) function to convert the SDDL string form to a security descriptor.</span></span>
4.  <span data-ttu-id="4b287-112">Используйте интерфейсы API безопасности [**жетсекуритидескриптордакл**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl), [**жетсекуритидескрипторсакл**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl), [**функций getsecuritydescriptorowner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)и [**жетсекуритидескрипторконтрол**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) для чтения частей дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="4b287-112">Use the [**GetSecurityDescriptorDacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl), [**GetSecurityDescriptorSacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl), [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner), and [**GetSecurityDescriptorControl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) Security APIs to read the parts of the security descriptor.</span></span>

<span data-ttu-id="4b287-113">Пример кода, демонстрирующий, как это сделать, см. в разделе [пример кода для чтения дефаултсекуритидескриптор](example-code-for-reading-defaultsecuritydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="4b287-113">For a code example that demonstrates how to do this, see [Example Code for Reading defaultSecurityDescriptor](example-code-for-reading-defaultsecuritydescriptor.md).</span></span>

 

 