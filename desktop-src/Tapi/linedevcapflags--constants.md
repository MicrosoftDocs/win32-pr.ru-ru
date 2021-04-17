---
description: '\_Константы битовой флага линедевкапфлагс — это коллекция логических значений, описывающих различные возможности устройств.'
ms.assetid: 0c537488-9fb9-4961-bd0a-1937aefc0b08
title: Константы LINEDEVCAPFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffefca75c00fdf09b1886affbff7f0ea90bab6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679880"
---
# <a name="linedevcapflags_-constants"></a>\_Константы линедевкапфлагс

Константы битовой флага **линедевкапфлагс \_** — это коллекция логических значений, описывающих различные возможности устройств.

<dl> <dt>

<span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**ЛИНЕДЕВКАПФЛАГС \_ каллхуб**
</dt> <dd> <dl> <dt>



Указывает, поддерживаются ли в этой строке концентраторы вызовов. Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 3,0 или более позднюю.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**ЛИНЕДЕВКАПФЛАГС \_ каллхубтраккинг**
</dt> <dd> <dl> <dt>



Указывает, поддерживается ли отслеживание концентратора вызовов в этой строке. Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 3,0 или более позднюю.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**ЛИНЕДЕВКАПФЛАГС \_ клоседроп**
</dt> <dd> <dl> <dt>



Указывает, что происходит, когда открытая строка закрывается, пока приложение вызывает активное в строке. Если **значение — true**, поставщик услуг сбрасывает (очищает) все активные вызовы в строке, когда последнее приложение, открывшее строку, закрывает его с помощью [**линеклосе**](/windows/desktop/api/Tapi/nf-tapi-lineclose). Если **значение равно false**, то поставщик услуг не удаляет активные вызовы в таких случаях. Вместо этого вызовы остаются активными и управляют внешними устройствами. Поставщик услуг обычно задает для этого бита **значение false** , если имеется другое устройство, которое может поддерживать вызов, например, если для аналоговой линии задано, что компьютер и телефон устанавливаются одновременно с подключением к ним в конфигурации, то телефон оффхук автоматически сохранит вызов активным даже после отключения компьютера.

Приложения должны установить этот флаг, чтобы определить, следует ли предупредить пользователя (с помощью диалогового окна ОК или Отмена), что активные вызовы будут потеряны.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**ЛИНЕДЕВКАПФЛАГС \_ кроссаддрконф**
</dt> <dd> <dl> <dt>



Указывает, можно ли выполнить конференцию для вызовов по разным адресам в этой строке.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**ЛИНЕДЕВКАПФЛАГС \_ диалбиллинг**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**ЛИНЕДЕВКАПФЛАГС \_ диалдиалтоне**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**ЛИНЕДЕВКАПФЛАГС \_ диалкуиет**
</dt> <dd> <dl> <dt>



Эти флаги указывают, поддерживается ли модификатор строки "$", "@" или "W", поддерживающий набор строк, для данного устройства линии. Имеет **значение true** , если модификатор поддерживается; в противном случае — **значение false**. "?" (предлагать пользователю продолжить набор) никогда не поддерживается линейным устройством. Эти флаги позволяют приложению определить, какие модификаторы приведут к созданию ЛИНИРР. Приложение имеет выбор предварительно сканируемых строк для неподдерживаемых символов или передачи "необработанных" строк из [**линетранслатеаддресс**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) непосредственно поставщику в составе таких функций, как [**линемакекалл**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) или [**линедиал**](/windows/desktop/api/Tapi/nf-tapi-linedial) , и позволить функции генерировать ошибку, чтобы сообщить ему, какой неподдерживаемый модификатор находится в строке первым.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**ЛИНЕДЕВКАПФЛАГС \_ хигхлевкомп**
</dt> <dd> <dl> <dt>



Указывает, поддерживаются ли в этой строке элементы сведений высокого уровня совместимости.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**ЛИНЕДЕВКАПФЛАГС \_ ловлевкомп**
</dt> <dd> <dl> <dt>



Указывает, поддерживаются ли в этой строке элементы сведений о совместимости низкого уровня.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**ЛИНЕДЕВКАПФЛАГС \_ медиаконтрол**
</dt> <dd> <dl> <dt>



Указывает, доступны ли операции управления мультимедиа для вызовов в этой строке.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**ЛИНЕДЕВКАПФЛАГС \_ MSP**
</dt> <dd> <dl> <dt>



Указывает, связана ли с линией поставщик службы мультимедиа (MSP). Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 3,0 или более позднюю.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**ЛИНЕДЕВКАПФЛАГС \_ мултиплеаддр**
</dt> <dd> <dl> <dt>



Указывает, могут ли [**линемакекалл**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**линедиал**](/windows/desktop/api/Tapi/nf-tapi-linedial), [**тспи \_ линемакекалл**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)или [**тспи \_ линедиал**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) работать с несколькими адресами одновременно (как для обратного мультиплексирования).


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**ЛИНЕДЕВКАПФЛАГС \_ приватеобжектс**
</dt> <dd> <dl> <dt>



Указывает, реализованы ли [интерфейсы, зависящие от поставщика](./provider-specific-interfaces.md) . Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 3,0 или более позднюю.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Без расширяемости. Все 32 бит зарезервированы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**линеклосе**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**линедиал**](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[**линемакекалл**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**линетранслатеаддресс**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)
</dt> </dl>

 

