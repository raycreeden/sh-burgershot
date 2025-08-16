# sh-burgershot
Job personalizado sumamente completo  y free
# Scripts pensados para Qb-core Frameworks  - 

- Dependencias  
- Qb-core - qb-banking - qb-policejob - qb-inventory

Las vestimentas no llamar a ningun script de ropa sino a las ropas entro del juego en cuestion, depende de sus pack de y como esten ubicados lo que se va a invocar. 

- La ropa femenina tiene sola una de las 2 prendas configuradas. 
- busquen la otra, en caso de tener pack de ropa antes de el pack estandar, es decir que el pack que agregaron se ponga antes que el pack del gta fivem por defecto se van a ver afectados los numeros de las prendas y deberan ubicarlos por su propia cuenta.

Estos scripts  estan pensandos para poder armar completamente gratis un servidor de qb-core y disfrutar de la experiencia sin perder calidad, sin embargo estoy aprendiendo y si bbien trato de que nada tenga errores puede que se vea mas rusticos que los ue hacen scripts populares.


# 1-  Qb-core - shared - Jobs
burgershot = {
    	label = "Vespucci BurgerShot",
    	defaultDuty = true,
		offDutyPay = false,
    	grades = {
        	['0'] = { name = "Empleado", payment = 50 },
        	['1'] = { name = "Supervisor", payment = 75 },
        	['2'] = { name = "Encargado", payment = 90 },
			['3'] = { name = "Subjefe", payment = 100 },
        	['4'] = { name = "jefe", isboss = true, payment = 130 },
    	},
	},
# 2-  Qb-Core - Shared.lua - Items
--Burgershot
    carne_cruda                  = { name = 'carne_cruda', label = 'Carne Cruda', weight = 500, type = 'item', image = 'carnecr.png', unique = false, useable = true, shouldClose = true, description = 'Carne Cruda' },
    carne_cocida                 = { name = 'carne_cocida', label = 'Carne Cocida', weight = 500, type = 'item', image = 'carnecoc.png', unique = false, useable = true, shouldClose = true, description = 'Carne Cruda' },    
    expr_frutilla                = { name = 'expr_frutilla', label = 'Exprimido Frutilla', weight = 100, type = 'item', image = 'exprfr.png', unique = false, useable = true, shouldClose = true, description = 'El Mas Rico de Todos', clientEvent = 'sh-burgershot:useConsumable' },
    expr_limon                   = { name = 'expr_limon', label = 'Exprimido Limon', weight = 100, type = 'item', image = 'exprlim.png', unique = false, useable = true, shouldClose = true, description = 'Exprimido de Limon', clientEvent = 'sh-burgershot:useConsumable' },
    hamb_doblecomp               = { name = 'hamb_doblecomp', label = 'Hamburguesa Doble Completa', weight = 400, type = 'item', image = 'hambdc.png', unique = false, useable = true, shouldClose = true, description = 'Esponjosa y Carnosa', clientEvent = 'sh-burgershot:useConsumable' },
    hamb_simple                  = { name = 'hamb_simple', label = 'Hamburguesa Simple', weight = 300, type = 'item', image = 'hambs.png', unique = false, useable = true, shouldClose = true, description = 'Rica Pero falta Carne', clientEvent = 'sh-burgershot:useConsumable' },
    hamb_vale                    = { name = 'hamb_vale', label = 'Vale Hamburguesa', weight = 100, type = 'item', image = 'hambvale.png', unique = false, useable = true, shouldClose = true, description = 'Intercambiar para retirar Hamburguesa al otro empleado' },
    hielo_sh                     = { name = 'hielo_sh', label = 'Hielos', weight = 200, type = 'item', image = 'hielosh.png', unique = false, useable = true, shouldClose = true, description = 'Hielo, si te metes uno entero en la boca, sos el Decimo Amigo' },
    hojas_lech                   = { name = 'hojas_lech', label = 'Hoja Lechuga', weight = 100, type = 'item', image = 'hojaslech.png', unique = false, useable = true, shouldClose = true, description = 'Hoja de Lechuga' },
    lechuga_sh                   = { name = 'lechuga_sh', label = 'Lechuga', weight = 200, type = 'item', image = 'lechugash.png', unique = false, useable = true, shouldClose = true, description = 'Una Planta de Lechuga sin Mas' },
    papa_cortada                 = { name = 'papa_cortada', label = 'Papa Cortada', weight = 200, type = 'item', image = 'papacortada.png', unique = false, useable = true, shouldClose = true, description = 'Papa Cortada' },
    papas_fr                     = { name = 'papas_fr', label = 'Papas Fritas', weight = 100, type = 'item', image = 'papasfr.png', unique = false, useable = true, shouldClose = true, description = 'Pero que Buenas Papas Fritas', clientEvent = 'sh-burgershot:useConsumable' },
    papa_sh                      = { name = 'papa_sh', label = 'Papa', weight = 300, type = 'item', image = 'papash.png', unique = false, useable = true, shouldClose = true, description = 'Papas' },
    sh_frutilla                  = { name = 'sh_frutilla', label = 'Frutillas', weight = 100, type = 'item', image = 'shfrut.png', unique = false, useable = true, shouldClose = true, description = 'Frutillas' },
    sh_limon                     = { name = 'sh_limon', label = 'Limones', weight = 100, type = 'item', image = 'shlim.png', unique = false, useable = true, shouldClose = true, description = 'Limones' },
    tomate_cort                  = { name = 'tomate_cort', label = 'Tomate Cortado', weight = 100, type = 'item', image = 'tomatecortado.png', unique = false, useable = true, shouldClose = true, description = 'Tomate Cortado' },
    tomate_sh                    = { name = 'tomate_sh', label = 'Tomate', weight = 200, type = 'item', image = 'tomatesh.png', unique = false, useable = true, shouldClose = true, description = 'Tomate Redondito' },
    burger_cafe                  = { name = 'burger_cafe', label = 'CafeShot', weight = 200, type = 'item', image = 'burgercafe.png', unique = false, useable = true, shouldClose = true, description = 'Cafe Perfecto', clientEvent = 'sh-burgershot:useConsumable' },
    agua_burger                  = { name = 'agua_burger', label = 'AguaShot', weight = 200, type = 'item', image = 'aguaburger.png', unique = false, useable = true, shouldClose = true, description = 'Agua de las Montañas del Himalaya', clientEvent = 'sh-burgershot:useConsumable' },
    refresco_bur                 = { name = 'refresco_bur', label = 'Refresco Burger', weight = 200, type = 'item', image = 'refrescobur.png', unique = false, useable = true, shouldClose = true, description = 'Refresco de Todos los Saboress', clientEvent = 'sh-burgershot:useConsumable' },


# 3- poner las imagenes dentro de qb-inventory images

# 4- Ensurar sh-burgershop 

# 5- cargar tabla
CREATE TABLE IF NOT EXISTS `burgershot_pedidos` (
    `id` INT AUTO_INCREMENT PRIMARY KEY,
    `citizenid` VARCHAR(50) NOT NULL,
    `item` VARCHAR(50) NOT NULL,
    `amount` INT NOT NULL,
    `timestamp` TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

CREATE TABLE IF NOT EXISTS `burgershot_movimientos` (
    `id` INT AUTO_INCREMENT PRIMARY KEY,
    `citizenid` VARCHAR(50) NOT NULL,
    `actorname` VARCHAR(100) DEFAULT NULL,
    `targetid` VARCHAR(50),
    `tipo` VARCHAR(50) NOT NULL,
    `cantidad` INT NOT NULL,
    `fecha` TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
  


-  Script.js qb-input modificado para que no de error en el anuncion pegarlo entero

let formInputs = {};

const OpenMenu = (data) => {
    if (data == null || data == "") {
        console.log("No data detected");
        return null;
    }

    $(`.main-wrapper`).fadeIn(0);

    let form = ["<form id='qb-input-form'>", `<div class="heading">${data.header != null ? data.header : "Form Title"}</div>`];

    data.inputs.forEach((item, index) => {
        switch (item.type) {
            case "text":
                form.push(renderTextInput(item));
                break;
            case "password":
                form.push(renderPasswordInput(item));
                break;
            case "number":
                form.push(renderNumberInput(item));
                break;
            case "radio":
                form.push(renderRadioInput(item));
                break;
            case "select":
                form.push(renderSelectInput(item));
                break;
            case "checkbox":
                form.push(renderCheckboxInput(item));
                break;
            case "color":
                form.push(renderColorInput(item));
                break;
            default:
                form.push(`<div class="label">${item.text}</div>`);
        }
    });

    form.push(`<div class="footer"><button type="submit" class="btn btn-success" id="submit">${data.submitText ? data.submitText : "Submit"}</button></div>`);

    form.push("</form>");
    
    // Limpiar estados previos y preparar el HTML
    const $wrapper = $(`.root-wrapper`);
    $wrapper.removeClass('hiding show');
    $(".main-wrapper").html(form.join(" "));

    // Mostrar el elemento pero manteniendo la posición inicial (fuera de pantalla)
    $wrapper.show();

    // Pequeño delay para asegurar que el DOM se ha actualizado, luego aplicar la animación
    setTimeout(() => {
        $wrapper.addClass('show');
    }, 10);

    // Configurar event listeners después de que el DOM esté listo
    setTimeout(() => {
        // Limpiar event listeners anteriores antes de agregar nuevos
        $("#qb-input-form").off("change").on("change", function (event) {
            if ($(event.target).attr("type") == "checkbox") {
                const value = $(event.target).is(":checked") ? "true" : "false";
                formInputs[$(event.target).attr("value")] = value;
            } else {
                formInputs[$(event.target).attr("name")] = $(event.target).val();
            }
        });

        $("#submit").off("click").on("click", async function (event) {
            if (event != null) {
                event.preventDefault();
            }
            await $.post(`https://${GetParentResourceName()}/buttonSubmit`, JSON.stringify({ data: formInputs }));
            CloseMenu();
        });
    }, 50);
};

const renderTextInput = (item) => {
    const { text, name } = item;
    formInputs[name] = item.default ? item.default : "";
    const isRequired = item.isRequired == "true" || item.isRequired ? "required" : "";
    const defaultValue = item.default ? `value="${item.default}"` : "";

    return ` <input placeholder="${text}" type="text" class="form-control" name="${name}" ${defaultValue} ${isRequired}/>`;
};

const renderPasswordInput = (item) => {
    const { text, name } = item;
    formInputs[name] = item.default ? item.default : "";
    const isRequired = item.isRequired == "true" || item.isRequired ? "required" : "";
    const defaultValue = item.default ? `value="${item.default}"` : "";

    return `<div><label for="${name}">${text}</label><input placeholder="${text}" type="password" class="form-control" name="${name}" ${defaultValue} ${isRequired}/></div>`;
};

const renderNumberInput = (item) => {
    try {
        const { text, name } = item;
        formInputs[name] = item.default ? item.default : "";
        const isRequired = item.isRequired == "true" || item.isRequired ? "required" : "";
        const defaultValue = item.default ? `value="${item.default}"` : "";

        return `<div><label for="${name}">${text}</label><input placeholder="${text}" type="number" class="form-control" name="${name}" ${defaultValue} ${isRequired}/></div>`;
    } catch (err) {
        console.log(err);
        return "";
    }
};

const renderRadioInput = (item) => {
    const { options, name, text } = item;
    formInputs[name] = options[0].value;

    let div = `<div class="form-input-group"> <div class="form-group-title">${text}</div>`;
    div += '<div class="input-group">';
    options.forEach((option, index) => {
        div += `<label for="radio_${name}_${index}"> <input type="radio" id="radio_${name}_${index}" name="${name}" value="${option.value}"
                ${(item.default ? item.default == option.value : index == 0) ? "checked" : ""}> ${option.text}</label>`;
    });

    div += "</div>";
    div += "</div>";
    return div;
};

const renderCheckboxInput = (item) => {
    const { options, name, text } = item;

    let div = `<div class="form-input-group"> <div class="form-group-title">${text}</div>`;
    div += '<div class="input-group-chk">';

    options.forEach((option, index) => {
        div += `<label for="chk_${name}_${index}">${option.text} <input type="checkbox" id="chk_${name}_${index}" name="${name}" value="${option.value}" ${option.checked ? "checked" : ""}></label>`;
        formInputs[option.value] = option.checked ? "true" : "false";
    });

    div += "</div>";
    div += "</div>";
    return div;
};

const renderSelectInput = (item) => {
    const { options, name, text } = item;
    let div = `<div class="select-title">${text}</div>`;

    div += `<select class="form-select" name="${name}" title="${text}">`;
    formInputs[name] = options[0].value;

    options.forEach((option, index) => {
        const isDefaultValue = item.default == option.value;
        div += `<option value="${option.value}" ${isDefaultValue ? "selected" : ""}>${option.text}</option>`;
        if (isDefaultValue) {
            formInputs[name] = option.value;
        }
    });
    div += "</select>";
    return div;
};

const renderColorInput = (item) => {
    const { text, name } = item;
    formInputs[name] = item.default ? item.default : "#ffffff";
    const isRequired = item.isRequired == "true" || item.isRequired ? "required" : "";
    const defaultValue = item.default ? `value="${item.default}"` : "";
    return `<div><label for="${name}">${text}</label><input placeholder="${text}" type="color" class="form-control" name="${name}" ${defaultValue} ${isRequired}/></div>`;
};

const CloseMenu = () => {
    $(`.main-wrapper`).fadeOut(0);
    $("#qb-input-form").remove();
    formInputs = {};
};

const SetStyle = (style) => {
    var stylesheet = $("<link>", {
        rel: "stylesheet",
        type: "text/css",
        href: `./styles/${style}.css`,
    });
    stylesheet.appendTo("head");
};

const CancelMenu = () => {
    $.post(`https://${GetParentResourceName()}/closeMenu`);
    return CloseMenu();
};

window.addEventListener("message", (event) => {
    const data = event.data;
    const info = data.data;
    const action = data.action;
    switch (action) {
        case "SET_STYLE":
            return SetStyle(info);
        case "OPEN_MENU":
            return OpenMenu(info);
        case "CLOSE_MENU":
            return CloseMenu();
        default:
            return;
    }
});

document.onkeyup = function (event) {
    const charCode = event.key;
    if (charCode == "Escape") {
        CancelMenu();
    } else if (charCode == "Enter") {
        // Enviar formulario al presionar Enter
        $("#submit").click();
    }
};

$(document).click(function (event) {
    var $target = $(event.target);
    if (!$target.closest(".main-wrapper").length && $(".root-wrapper").hasClass("show")) {
        CancelMenu();
    }
});
