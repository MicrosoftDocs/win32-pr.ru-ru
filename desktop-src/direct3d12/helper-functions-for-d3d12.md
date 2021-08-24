---
title: Вспомогательные функции для Direct3D 12
description: Эти вспомогательные функции помогают в частности обрабатывать подресурсы и объявляются в `d3dx12.h` .
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Вспомогательные функции
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9434bf916d7cb92116cdf4f7f6d86363b2eb51
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813190"
---
# <a name="helper-functions-for-direct3d-12"></a>Вспомогательные функции для Direct3D 12

Эти вспомогательные функции помогают в частности обрабатывать подресурсы и объявляются в `d3dx12.h` .

`d3dx12.h` доступен отдельно от заголовков Direct3D 12. Вы можете скачать `d3dx12.h` из [вспомогательной библиотеки D3D12](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h).

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
|-|-|
| [**CommandListCast**](commandlistcast.md) | Этот шаблон функции приводит указатель константы к любому списку команд в указатель const на ID3D12CommandList. |
| [**D3D12CalcSubresource**](d3d12calcsubresource.md) | Вычисляет индекс подресурсов для текстуры. |
| [**D3D12DecomposeSubresource**](d3d12decomposesubresource.md) | Выводит срез MIP, срез массива и срез, соответствующие указанному индексу подресурса. |
| [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) | Возвращает число плоскостей для указанного формата DXGI для указанного виртуального адаптера ( **ID3D12Device**). |
| [**D3D12IsLayoutOpaque**](d3d12islayoutopaque.md) | Указывает, является ли макет непрозрачным. |
| [**D3DX12GetBaseSubobjectType**](d3dx12getbasesubobjecttype.md) | Возвращает тип подобъекта, соответствующий базовому классу переданного типа подобъекта. |
| [**D3DX12ParsePipelineStateStream**](d3dx12parsepipelinestream.md) | Анализирует описание потока состояния конвейера, вызывая пользовательский обратный вызов для каждого анализируемого экземпляра подобъекта. |
| [**D3DX12SerializeVersionedRootSignature**](d3dx12serializeversionedrootsignature.md) | Помогает включить функции корневой подписи 1,1, когда они доступны, и не требует поддержки двух путей кода для сборки корневых подписей. Этот вспомогательный метод восстанавливает корневую подпись версии 1,0, если версия 1,1 не поддерживается. |
| [**GetRequiredIntermediateSize**](getrequiredintermediatesize.md) | Возвращает требуемый размер буфера, используемый для передачи данных. |
| [**Memcpysubresource**](memcpysubresource.md) | Копирует подресурс по строкам. |
| [**Updatesubresources**](updatesubresources1.md) | Обновляет подресурсы, все массивы подресурсов должны быть заполнены, обычно путем вызова [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints). |
| [**Updatesubresources (выделение кучи)**](updatesubresources2.md) | Обновляет подресурсы с реализацией выделения кучи. |
| [**Updatesubresources (выделение стека)**](updatesubresources3.md) | Обновляет подресурсы с реализацией выделения стека. |

## <a name="related-topics"></a>Связанные темы

* [Справочник по Direct3D 12](direct3d-12-reference.md)
* [Вспомогательные структуры и функции для D3D12](helper-structures-and-functions-for-d3d12.md)
