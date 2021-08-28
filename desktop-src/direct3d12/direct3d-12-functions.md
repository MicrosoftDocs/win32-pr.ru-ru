---
title: Основные функции (графика Direct3D 12)
description: Следующие функции объявляются в d3d12. h.
ms.assetid: C0F9A52C-483D-40B2-9E1F-CB92ADDC2856
ms.localizationpriority: low
ms.topic: article
ms.date: 11/27/2018
ms.openlocfilehash: e38145bc4aef4c07ba00de4185fc97ad449f4f2c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881791"
---
# <a name="core-functions"></a>Базовые функции

Следующие функции объявляются в d3d12. h.

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
|-|-|
| [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) | Создает устройство, представляющее адаптер дисплея. |
| [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) | Десериализует корневую подпись, чтобы можно было определить Определение макета ([**D3D12 \_ корневая \_ сигнатура \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)). |
| [**D3D12CreateVersionedRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createversionedrootsignaturedeserializer) | Создает интерфейс, который может возвращать десериализованную структуру данных через [**жетунконвертедрутсигнатуредеск**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc). |
| [**D3D12EnableExperimentalFeatures**](/windows/desktop/api/d3d12/nf-d3d12-d3d12enableexperimentalfeatures) | Включает список экспериментальных функций. |
| [**D3D12GetDebugInterface**](/windows/desktop/api/d3d12/nf-d3d12-d3d12getdebuginterface) | Возвращает интерфейс отладки. |
| [**D3D12GetInterface**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) | выбирает версию пакета SDK во время выполнения, когда система находится в Windows режиме разработчика. |
| [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature) | Сериализует корневую подпись версии 1,0, которую можно передать в [**ID3D12Device:: креатерутсигнатуре**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature). |
| [**D3D12SerializeVersionedRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) | Сериализует корневую подпись любой версии, которую можно передать в [**ID3D12Device:: креатерутсигнатуре**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature). |

## <a name="related-topics"></a>Связанные темы

* [Справочник по коду](direct3d-12-core-reference.md)
* [Справочник по Direct3D 12](direct3d-12-reference.md)
