---
title: Многопоточные проблемы
description: Многопоточные проблемы
ms.assetid: 17e74d2a-af4f-4188-89fa-b4f50abc424f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ffd1dc3f73c33ca30ebee0072f1c5059c73f25e9e2318d384cd0c3d0dc7bc94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117918534"
---
# <a name="multi-threaded-issues"></a>Многопоточные проблемы

Технология OLE обеспечивает поддержку многопоточных приложений, позволяя приложениям выполнять вызовы OLE из нескольких потоков. Эта Многопотоковая поддержка называется моделью подразделения, поэтому важно, чтобы все компоненты OLE, использующие несколько потоков, следовали этой модели. Для модели апартамента необходимо, чтобы указатели интерфейса были упакованы (с использованием [**комаршалинтерфаце**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)и [**каунмаршалинтерфаце**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)) при передаче между потоками.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Процессы, потоки и подразделения](processes--threads--and-apartments.md)
</dt> </dl>

 

 




