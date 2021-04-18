---
title: Элемент install
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Элемент Install указывает значения, используемые проигрывателем Windows Media для установки Интернет-магазина.
ms.assetid: 9a5e15ee-ec36-48d3-a1c2-bf20b6d2da48
keywords:
- Установка элемента Windows Media Player
topic_type:
- apiref
api_name:
- Install Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bba56240651f789b45c18b006b16e5e07b10676e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694659"
---
# <a name="install-element"></a>Элемент install

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Элемент **Install** указывает значения, используемые проигрывателем Windows Media для установки Интернет-магазина.

``` syntax
<Install
    EULAURL = "URL"
    CodeURL = "URL"
    PrivacyInfoURL = "URL"
    InstallApp = "filename"
    InstallData = "commandline"
    CatalogURL = "URL"
/>
```

## <a name="attributes"></a>Атрибуты

<dl> <dt>

<span id="EULAURL__required_"></span><span id="eulaurl__required_"></span><span id="EULAURL__REQUIRED_"></span>**Еулаурл** (обязательно)
</dt> <dd>

Полный URL-адрес для файла с расширением txt, используемым проигрывателем Windows Media для вывода лицензионного соглашения (EULA). Этот файл должен быть закодирован в формате ANSI.

</dd> <dt>

<span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**Кодеурл** (обязательно)
</dt> <dd>

Полный URL-адрес пакета с расширением CAB, который используется для установки Интернет-магазина. Пакет и все модули кода в пакете должны быть подписаны. Сведения о подписывании кода см. в статье [Введение в подписывание кода](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) в библиотеке MSDN.

</dd> <dt>

<span id="PrivacyInfoURL__required_"></span><span id="privacyinfourl__required_"></span><span id="PRIVACYINFOURL__REQUIRED_"></span>**Привациинфаурл** (обязательно)
</dt> <dd>

Полный URL-адрес веб-страницы, содержащей сведения о политике конфиденциальности для Интернет-магазина.

</dd> <dt>

<span id="InstallApp__required_"></span><span id="installapp__required_"></span><span id="INSTALLAPP__REQUIRED_"></span>**Инсталлапп** (обязательно)
</dt> <dd>

Имя запускаемого EXE-или INF-файла. Этот файл должен содержаться в CAB-файле, указанном атрибутом **кодеурл** .

</dd> <dt>

<span id="InstallData__optional_"></span><span id="installdata__optional_"></span><span id="INSTALLDATA__OPTIONAL_"></span>**Инсталлдата** (необязательно)
</dt> <dd>

Строка командной строки, которая передается в приложение, указанное атрибутом **инсталлапп** . Этот атрибут применим только в том случае, если значение параметра **инсталлапп** указывает исполняемый файл.

</dd> <dt>

<span id="CatalogURL__required_for_type_1__ignored_for_type_2_"></span><span id="catalogurl__required_for_type_1__ignored_for_type_2_"></span><span id="CATALOGURL__REQUIRED_FOR_TYPE_1__IGNORED_FOR_TYPE_2_"></span>**Каталогурл** (требуется для типа 1, игнорируется для типа 2)
</dt> <dd>

Полный URL-адрес для скомпилированного каталога Интернет-магазина.

</dd> </dl>

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия       | Элемент         |
|-----------------|-----------------|
| Родительские элементы | **ServiceInfo** |
| Дочерние элементы  | Нет            |



 

## <a name="remarks"></a>Remarks

Если какой-либо из необходимых атрибутов отсутствует или недоступен, программа установки проигрывателя Windows Media не будет пытаться загрузить и установить код поставщика интерактивного магазина. Программа установки настроит значения автономного режима по умолчанию, как указано в документе **serviceInfo** . **ServiceInfo** можно использовать при отсутствии подключения к Интернету, передав имя поставщика по умолчанию и сведения о **serviceInfo** в качестве параметров командной строки. Дополнительные сведения о параметрах командной строки см. в разделе [распространение программного обеспечения проигрывателя Windows Media](redistributing-windows-media-player-software.md) .

> [!Note]  
> Для использования этого элемента необходимо подписать соглашение о повторном распространении с помощью корпорации Майкрософт. Для получения дополнительных сведений обратитесь к своему бизнес-представителям.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 10 или более поздней версии.<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Пример документа ServiceInfo для Интернет-магазина типа 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Пример документа ServiceInfo для Интернет-магазина типа 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Документ ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

