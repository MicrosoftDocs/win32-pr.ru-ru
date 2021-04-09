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
# <a name="reading-the-defaultsecuritydescriptor-for-an-object-class"></a>Чтение Дефаултсекуритидескриптор для класса Object

С помощью ADSI можно получить атрибут **дефаултсекуритидескриптор** для класса объекта с помощью интерфейса [**iAds**](/windows/desktop/api/iads/nn-iads-iads) . Чтобы получить атрибут **дефаултсекуритидескриптор** для класса объекта, выполните следующие действия.

1.  Получите указатель интерфейса [**iAds**](/windows/desktop/api/iads/nn-iads-iads) на объект **classSchema** для класса Object.
2.  Используйте метод [**iAds. Get**](/windows/desktop/api/iads/nf-iads-iads-get) , чтобы получить дескриптор безопасности объекта по умолчанию. Имя свойства, содержащего дескриптор безопасности, — "Дефаултсекуритидескриптор". Свойство будет возвращено как [**значение типа Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) , содержащее BSTR с дескриптором безопасности по умолчанию в формате строки SDDL.
3.  Используйте функцию [**конвертстрингсекуритидескриптортосекуритидескриптор**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) , чтобы преобразовать форму строки SDDL в дескриптор безопасности.
4.  Используйте интерфейсы API безопасности [**жетсекуритидескриптордакл**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl), [**жетсекуритидескрипторсакл**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl), [**функций getsecuritydescriptorowner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)и [**жетсекуритидескрипторконтрол**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) для чтения частей дескриптора безопасности.

Пример кода, демонстрирующий, как это сделать, см. в разделе [пример кода для чтения дефаултсекуритидескриптор](example-code-for-reading-defaultsecuritydescriptor.md).

 

 