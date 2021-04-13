---
title: Реализация и активация обработчика с дополнительными данными, предоставляемыми сервером
description: Реализация и активация обработчика с дополнительными данными, предоставляемыми сервером
ms.assetid: 5bbf81bd-430d-4008-b1cc-9ea91bb3b1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db78a3e39c85c37c52dfa3f09ef41f0a71b5f431
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "104350865"
---
# <a name="implementing-and-activating-a-handler-with-extra-data-supplied-by-server"></a>Реализация и активация обработчика с дополнительными данными, предоставляемыми сервером

Если сервер хочет включить в пакет некоторые дополнительные данные для использования обработчика, на сервере должны быть реализованы интерфейсы [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) и [**истдмаршалинфо**](/windows/win32/api/objidlbase/nn-objidlbase-istdmarshalinfo) . Сервер должен выполнить статистическую обработку стандартного модуля упаковки и делегировать первую часть упаковки в агрегированный стандартный модуль упаковки, включая [**IMarshal:: жетунмаршалкласс**](/windows/desktop/api/ObjIdl/nf-objidl-imarshal-getunmarshalclass), и должен добавить свой собственный размер данных в размер, возвращенный [**IMarshal:: GetMarshalSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-imarshal-getmarshalsizemax)стандартного маршалером. Стандартный модуль упаковки вызывает [**истдмаршалинфо:: жетклассфорхандлер**](/windows/win32/api/objidlbase/nf-objidlbase-istdmarshalinfo-getclassforhandler) , чтобы получить идентификатор CLSID создаваемого обработчика. После завершения маршалирования стандартного модуля упаковки сервер записывает в поток собственные дополнительные данные. Итоговые структуры с дополнительными данными в потоке показаны на следующем рисунке:

![Схема, в которой показаны структуры с дополнительными данными в потоке.](images/4cff306b-bb82-4c05-8e64-7ca73731f265.png)

## <a name="server-side-structures-with-extra-data-in-stream"></a>Server-Side структур с дополнительными данными в потоке

Это позволяет вызову из COM [**каунмаршалинтерфаце**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) на стороне клиента возможность пропустить все непрочитанные данные и оставить поток в соответствующей строке после всех данных упакованного интерфейса, если обработчик не может быть создан.

## <a name="client-side-structures-with-extra-data-in-stream"></a>Client-Side структур с дополнительными данными в потоке

Как и в случае, когда в потоке нет дополнительных данных сервера, вызов COM на стороне клиента в [**каунмаршалинтерфаце**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) создаст удостоверение и обработчик. Обработчик должен реализовать [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) и должен сначала делегировать вызовы **IMarshal** агрегированному стандартному маршалеру, а затем маршалировать или распаковать любые дополнительные данные, предоставленные сервером. [**Унмаршалинтерфаце**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-unmarshalinterface) обработчика будет вызываться для каждого распаковки, независимо от того, был ли он размаршалирован перед или нет. В этом случае сервер не вызывает [**кожетстдмаршалекс**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex) , но обработчик должен. Итоговая структура на стороне клиента показана на следующем рисунке.

![Схема, на которой показана структура на стороне клиента.](images/053411c7-9d54-4ae5-bcb6-778454b1d86f.png)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Упрощенный обработчик Client-Side](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 