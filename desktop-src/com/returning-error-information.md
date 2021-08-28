---
title: Возврат сведений об ошибке
description: Возврат сведений об ошибке
ms.assetid: 4206f2e5-db01-458c-93cb-10c5cd4a4536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545c697be7da64362ecce0f5b4c45272832ad682d8b4dd0eb5234620b993e5f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309646"
---
# <a name="returning-error-information"></a>Возврат сведений об ошибке

Используя интерфейсы и функции обработки ошибок COM, вы можете вернуть сведения об ошибке, выполнив следующие действия:

1.  Реализуйте интерфейс [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) .
2.  Чтобы создать экземпляр общего объекта Error, вызовите функцию [**креатирроринфо**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo) .
3.  Чтобы задать его содержимое, используйте методы [**икреатирроринфо**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo) .
4.  Чтобы связать объект Error с текущим логическим потоком, вызовите функцию [**сетерроринфо**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) .

Интерфейсы обработки ошибок создают и управляют объектом Error, который предоставляет сведения об ошибке. Объект ошибки не совпадает с объектом, в котором произошла ошибка. Это отдельный объект, связанный с текущим потоком выполнения.

 

 