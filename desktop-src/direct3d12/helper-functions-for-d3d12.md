---
title: Вспомогательные функции для D3D12
description: Эти вспомогательные функции помогают в частности обрабатывать подресурсы и объявляются в d3dx12. h.
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Вспомогательные функции
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10736d91da0e2c4efa2a3c981ab5c4f64e2af86d
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102142"
---
# <a name="helper-functions-for-d3d12"></a>Вспомогательные функции для D3D12

Эти вспомогательные функции помогают в частности обрабатывать подресурсы и объявляются в **d3dx12. h**.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                             | Описание                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommandListCast**](commandlistcast.md)<br/>                                     | Этот шаблон функции приводит указатель константы к любому списку команд в указатель const на ID3D12CommandList.<br/>                                                                                                                               |
| [**D3D12CalcSubresource**](d3d12calcsubresource.md)<br/>                                   | Вычисляет индекс подресурсов для текстуры. <br/>                                                                                                                                                                                                  |
| [**D3D12DecomposeSubresource**](d3d12decomposesubresource.md)<br/>                         | Выводит срез MIP, срез массива и срез, соответствующие указанному индексу подресурса. <br/>                                                                                                                                        |
| [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md)<br/>                           | Возвращает число плоскостей для указанного формата DXGI для указанного виртуального адаптера ( **ID3D12Device**). <br/>                                                                                                                               |
| [**D3D12IsLayoutOpaque**](d3d12islayoutopaque.md)<br/>                                     | Указывает, является ли макет непрозрачным.<br/>                                                                                                                                                                                                         |
| [**D3DX12GetBaseSubobjectType**](d3dx12getbasesubobjecttype.md)<br/>                       | Возвращает тип подобъекта, соответствующий базовому классу переданного типа подобъекта.<br/>                                                                                                                                                  |
| [**D3DX12ParsePipelineStateStream**](d3dx12parsepipelinestream.md)<br/>                    | Анализирует описание потока состояния конвейера, вызывая пользовательский обратный вызов для каждого анализируемого экземпляра подобъекта.<br/>                                                                                                                                 |
| [**D3DX12SerializeVersionedRootSignature**](d3dx12serializeversionedrootsignature.md)<br/> | Помогает включить функции корневой подписи 1,1, когда они доступны, и не требует поддержки двух путей кода для сборки корневых подписей. Этот вспомогательный метод восстанавливает корневую подпись версии 1,0, если версия 1,1 не поддерживается.<br/> |
| [**GetRequiredIntermediateSize**](getrequiredintermediatesize.md)<br/>                     | Возвращает требуемый размер буфера, используемый для передачи данных. <br/>                                                                                                                                                                              |
| [**Memcpysubresource**](memcpysubresource.md)<br/>                                         | Копирует подресурс по строкам. <br/>                                                                                                                                                                                                               |
| [**Updatesubresources**](updatesubresources1.md)<br/>                                      | Обновляет подресурсы, все массивы подресурсов должны быть заполнены, обычно путем вызова [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints). <br/>                                                                  |
| [**Updatesubresources (выделение кучи)**](updatesubresources2.md)<br/>                    | Обновляет подресурсы с реализацией выделения кучи. <br/>                                                                                                                                                                                    |
| [**Updatesubresources (выделение стека)**](updatesubresources3.md)<br/>                   | Обновляет подресурсы с реализацией выделения стека. <br/>                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по Direct3D 12](direct3d-12-reference.md)
</dt> <dt>

[Вспомогательные структуры и функции для D3D12](helper-structures-and-functions-for-d3d12.md)
</dt> </dl>

 

 





