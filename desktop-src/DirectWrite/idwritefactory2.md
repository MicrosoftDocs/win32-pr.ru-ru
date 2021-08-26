---
title: Интерфейс IDWriteFactory2
description: интерфейс корневой фабрики для всех объектов DirectWrite.
ms.assetid: 1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE
keywords:
- Непосредственная запись интерфейса IDWriteFactory1
- Непосредственная запись интерфейса IDWriteFactory1, описание
topic_type:
- apiref
api_name:
- IDWriteFactory1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370292387f2c42e3f749e24a063e05bb24280ec5c8e8941a430f996fe7f349da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902804"
---
# <a name="idwritefactory2-interface"></a>Интерфейс IDWriteFactory2

интерфейс корневой фабрики для всех объектов [DirectWrite](direct-write-portal.md) .

## <a name="members"></a>Элементы

Интерфейс **IDWriteFactory1** наследует от [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1). **IDWriteFactory2** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **IDWriteFactory1** содержит следующие методы.



| Метод                                                                             | Описание                                                                                                |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**креатекустомрендерингпарамс**](idwritefactory2-createcustomrenderingparams.md) | Создает объект параметров отрисовки с указанными свойствами.<br/>                            |
| [**креатефонтфаллбаккбуилдер**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-createfontfallbackbuilder)     | Создает объект построителя шрифтов.<br/>                                                         |
| [**креатеглифрунаналисис**](idwritefactory2-createglyphrunanalysis.md)           | Создает объект анализа выполнения глифа, который инкапсулирует сведения, используемые для визуализации выполнения глифа.<br/> |
| [**жетсистемфонтфаллбакк**](idwritefactory2-getsystemfontfallback.md)             | Создает резервный объект шрифта из списка резервных шрифтов системы.<br/>                              |
| [**транслатеколорглифрун**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun)           | Этот метод вызывается для выполнения глифа, чтобы перевести его в несколько цветовых глифов.<br/>           |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ приложения UWP для классических приложений \|\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Server 2012 Приложения универсального \[ приложения UWP для настольных приложений \|\]<br/>                          |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/> |
| Библиотека<br/>                  | <dl> <dt>Дврите. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1)
</dt> <dt>

[**идвритефактори**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)
</dt> </dl>

 

