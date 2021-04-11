---
title: Получение информации об ошибке
description: Получение информации об ошибке
ms.assetid: 51a0e401-43f2-4738-9799-a96e2580a29f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a5918ee7338d1b8428079da20ecb43c7b4b4ef
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070651"
---
# <a name="retrieving-error-information"></a>Получение информации об ошибке

Используя интерфейсы и функции обработки ошибок COM, можно получить сведения об ошибке следующим образом:

1.  Проверьте, представляет ли возвращаемое значение ошибку, которую объект готов к обработке.
2.  Вызовите [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) , чтобы получить указатель на интерфейс [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) . Затем вызовите метод [**ISupportErrorInfo:: интерфацесуппортсерроринфо**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) , чтобы убедиться, что ошибка была вызвана объектом, который его вернул, а объект Error относится к текущей ошибке, а не к предыдущему вызову.
3.  Чтобы получить указатель на объект Error, вызовите функцию [**жетерроринфо**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) .
4.  Чтобы получить сведения из объекта Error, используйте методы [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .

Если объект не готов к обработке ошибки, но ему необходимо распространить сведения об ошибке дальше по цепочке вызовов, он должен просто передать возвращаемое значение вызывающему объекту. Поскольку функция [**жетерроринфо**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) удаляет сведения об ошибке и передает владение объекту-ошибке вызывающему объекту, функция должна вызываться только объектом, обрабатывающим ошибку.

 

 