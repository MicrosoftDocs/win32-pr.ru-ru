---
title: Коды возврата Direct3D 11
description: Коды возврата из функций API.
ms.assetid: c0856a58-b760-44e5-8acf-145720b403d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d932c3ce3828f375e90bf322af6c42dc112b845f44dfe22f0d0988930129efea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990044"
---
# <a name="direct3d-11-return-codes"></a>Коды возврата Direct3D 11

Коды возврата из функций API.

| HRESULT | Описание |
|-|-|
| D3D11_ERROR_FILE_NOT_FOUND (0x887C0002) | Файл не найден. |
| D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS (0x887C0001) | Слишком много уникальных экземпляров определенного типа объекта состояния. |
| D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS (0x887C0003) | Слишком много уникальных экземпляров определенного типа объекта представления. |
| D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD (0x887C0004) | Первый вызов [**ссылку ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) после либо [**ID3D11Device:: Креатедеферредконтекст**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext) , либо [**ссылку ID3D11DeviceContext:: финишкоммандлист**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) на ресурс не D3D11_MAP_WRITE_DISCARD. |
| D3DERR_INVALIDCALL (заменяется на DXGI_ERROR_INVALID_CALL) (0x887A0001) | Недопустимый вызов метода. Например, параметр метода не может быть допустимым указателем. |
| D3DERR_WASSTILLDRAWING (заменяется на DXGI_ERROR_WAS_STILL_DRAWING) (0x887A000A) | Предыдущая операция Блит, которая передает информацию в эту область или из нее, является неполной. |
| E_FAIL (0x80004005) | Попытка создать устройство с включенным уровнем отладки, и этот слой не установлен. |
| E_INVALIDARG (0x80070057) | Функции, возвращающей, передан недопустимый параметр. |
| E_OUTOFMEMORY (0x8007000E) | Direct3D не удалось выделить достаточно памяти для завершения вызова. |
| E_NOTIMPL (0x80004001) | Вызов метода не реализован с переданным сочетанием параметров. |
| S_FALSE ((HRESULT) 1L) | Альтернативное значение успеха, указывающее на успешное, но нестандартное завершение (точное значение зависит от контекста). |
| S_OK ((HRESULT) 0L) | Без ошибок. |

Дополнительные коды возврата см. в разделе [DXGI_ERROR](/windows/desktop/direct3ddxgi/dxgi-error).

## <a name="related-topics"></a>Связанные темы

* [Справочник по Direct3D 11](d3d11-graphics-reference.md)