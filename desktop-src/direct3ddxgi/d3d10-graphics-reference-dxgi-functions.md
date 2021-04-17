---
description: В этом разделе содержатся сведения о функциях, предоставляемых DXGI.
ms.assetid: 209d2e65-b118-47a7-aece-fb140fdede3f
title: Функции DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06cb98c47ec3e2cb841aa5c27017ee6bb614f9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536809"
---
# <a name="dxgi-functions"></a>Функции DXGI

В этом разделе содержатся сведения о функциях, предоставляемых DXGI.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                   | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**креатедксгифактори**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory)<br/>                               | Создает фабрику DXGI 1,0, которую можно использовать для создания других объектов DXGI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**CreateDXGIFactory1**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1)<br/>                             | Создает фабрику DXGI 1,1, которую можно использовать для создания других объектов DXGI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2)<br/>                             | Создает фабрику DXGI 1,3, которую можно использовать для создания других объектов DXGI.<br/> В Windows 8 любая фабрика DXGI, созданная при наличии DXGIDebug.dll в системе, будет загружать и использовать ее. Начиная с Windows 8.1, приложения явно запрашивают, что DXGIDebug.dll быть загружены. Используйте [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) и укажите \_ \_ флаг создания отладочной фабрики DXGI \_ , чтобы запросить DXGIDebug.dll. Библиотека DLL будет загружена, если она есть в системе.<br/> |
| [**дксгидеклареадаптерремовалсуппорт**](/windows/desktop/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport)<br/> | Позволяет процессу указать, что он устойчив к любому удаляемому графическому устройству.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**дксгижетдебугинтерфаце**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)<br/>                       | Извлекает интерфейс отладки.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**DXGIGetDebugInterface1**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-dxgigetdebuginterface1)<br/>                     | Извлекает интерфейс, используемый приложениями Магазина Windows для отладки графической инфраструктуры Microsoft DirectX (DXGI).<br/>                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Ссылка на DXGI](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

 




