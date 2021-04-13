---
title: Многопоточные проблемы
description: Многопоточные проблемы
ms.assetid: 17e74d2a-af4f-4188-89fa-b4f50abc424f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0910e1602d00d3429bb9e4c7a1667bf8113cd659
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411462"
---
# <a name="multi-threaded-issues"></a>Многопоточные проблемы

Технология OLE обеспечивает поддержку многопоточных приложений, позволяя приложениям выполнять вызовы OLE из нескольких потоков. Эта Многопотоковая поддержка называется моделью подразделения, поэтому важно, чтобы все компоненты OLE, использующие несколько потоков, следовали этой модели. Для модели апартамента необходимо, чтобы указатели интерфейса были упакованы (с использованием [**комаршалинтерфаце**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)и [**каунмаршалинтерфаце**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)) при передаче между потоками.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Процессы, потоки и подразделения](processes--threads--and-apartments.md)
</dt> </dl>

 

 




