---
title: Элемент install
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. элемент Install указывает значения, используемые проигрыватель Windows Media для установки интернет-магазина.
ms.assetid: 9a5e15ee-ec36-48d3-a1c2-bf20b6d2da48
keywords:
- элемент установки проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Install Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05a946cbab6a6334faa7483c0f3201a98ff0abe32dca32fe1f4f7eed5d0a2408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996524"
---
# <a name="install-element"></a>Элемент install

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

элемент **Install** указывает значения, используемые проигрыватель Windows Media для установки интернет-магазина.

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

полный URL-адрес для файла с .txt расширением имени файла, которое проигрыватель Windows Media использует для вывода лицензионного соглашения (EULA). Этот файл должен быть закодирован в формате ANSI.

</dd> <dt>

<span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**Кодеурл** (обязательно)
</dt> <dd>

Полный URL-адрес пакета с .cab расширением имени файла, который используется для установки Интернет-магазина. Пакет и все модули кода в пакете должны быть подписаны. сведения о подписывании кода см. в разделе [введение в подписывание кода](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) в библиотека MSDN.

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

если какой-либо из необходимых атрибутов отсутствует или недоступен, проигрыватель Windows Media программа установки не будет пытаться загрузить и установить код поставщика интерактивного магазина. Программа установки настроит значения автономного режима по умолчанию, как указано в документе **serviceInfo** . **ServiceInfo** можно использовать при отсутствии подключения к Интернету, передав имя поставщика по умолчанию и сведения о **serviceInfo** в качестве параметров командной строки. дополнительные сведения о параметрах командной строки см. в разделе [распространение проигрыватель Windows Media программное обеспечение](redistributing-windows-media-player-software.md) .

> [!Note]  
> Для использования этого элемента необходимо подписать соглашение о повторном распространении с помощью корпорации Майкрософт. Для получения дополнительных сведений обратитесь к своему бизнес-представителям.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 10 или более поздней версии.<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Пример документа ServiceInfo для Интернет-магазина типа 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Пример документа ServiceInfo для Интернет-магазина типа 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Документ ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

