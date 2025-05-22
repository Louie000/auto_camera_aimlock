# auto_camera_aimlock

Citizen.CreateThread(function()
    local Timea = 800
    while true do
        Citizen.Wait(Timea)
        local playerPed = PlayerPedId()
        local weapon = GetSelectedPedWeapon(playerPed)
        if weapon ~= `WEAPON_UNARMED` then
            Timea = 0
            if IsPlayerFreeAiming(PlayerId()) then
                if GetFollowPedCamViewMode() ~= 4 then
                    SetFollowPedCamViewMode(4)
                end
            else
                if GetFollowPedCamViewMode() ~= 1 then
                    SetFollowPedCamViewMode(1)
                end
                --DisableControlAction(0, 24, true) -- ปิดยิงซ้ายเมาส์
                --DisableControlAction(0, 25, true) -- ปิดยิงขวาเมาส์
                DisablePlayerFiring(playerPed, true)
            end
        else
            Timea = 800
        end
    end
end)
